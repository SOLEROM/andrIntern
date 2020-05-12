# systemServer

* functions as the service host process, wherein most services are implemented as threads

## about
* framework services are simple enough that they do not require their own process, and can instead run as threads
* These threads,however, need a host process to run in - and that is exactly what system_server provides
* systemServer provides nothing more than a shell - a container process
* systemServer loads Java classes
* only Android's system services, and not those of the vendor or additional apps, are allowed to run inside system_server
* system_server is not a native app: It is implemented mostly in Java, with some JNI calls in places where it must start native service
* Zygote automatically starts the system_server when it itself is started by the /init.rc



## calling pattern
* Android's framework services are implemented in systemServer threads
* rely on Inter-Process Communication (IPC) in order to invoke
* using the Binder, Android's properietary IPC mechanism
* Applications need to call on the Binder in their own process 
* that will obtain an endpoint descriptor connected to the remote service
* Methods then be invoked through IPC messages, through a pattern known as Remote Procedure Call (RPC)
* get to know [RPC](rpc.md) pattern



## Startup
* forked off from Zygote
* the child process drops its privileges, and toggles the capabilities
* proceeds to load the class
* main performs basic initialization
* perform JNI component initialization
* instantiating the framework services
* create all services - spun threads
* the main thread enters a looper


* system services to start instantiated one by one
* grouping services of similar classification
	* Bootstrap services
	* Core services
	* "Other" services: basically, everything else


## Modifying startup behavior
* can be modified by setting certain system properties

### ro.factorygtest
* defines whether or not the device is configured for a "factory test" mode
* affecting the startup of system server:

```
0 (default) 	FACTORY_TEST_NONE 		Normal startup.
1 		FACTORY_TEST_LOW_LEVEL		No bluetooth, input, accessibility, lock settings
2 		FACTORY_TEST_HIGH_LEVEL 	Uid 0 for factory test applications
```

### ro.headless
* if set - disables the WallPaper service, and the System UI services

### config
* properties can also be used to selectively disable subsystems

```
disable_storage 	MountService
disable_media 		AudioService,WiredAccessoryManager, CommonTimeManagementService
disable_bluetooth 	BluetoothManagerService
disable_telephony 	Unused
disable_location 	LocationManagerService, CountryDetectorService
disable_systemui 	StatusBarManagerService

disable_noncore 	UpdateLockService, LockSettingsService, TextServicesManager,
			SearchManagerService, WallpaperManagerService, DockObserver, UsbService

disable_network 	NetworkStatsService,NetworkPolicyManagerService,WifiP2pService,
			WifiService,ConnectivityService,
			NsdService,NetworkTimeUpdateService,CertBlacklister
```


 
