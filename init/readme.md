# init

* Android init , however, is vastly different than that of UN*X or Linux
* mainly support of System Properties and using a particular set of rc files
* also implemented by init are ueventd and watchdogd, loaded through a symbolic link.

* As a binary, /init is statically linked - all of its dependencies are merged into the binary during compilation
* mitigate the risk that a corrupt or missing library abort system startup

* on first launched, the only filesystem mounted is the root filesystem (i.e / and /sbin )
* which is packaged in the Android boot partition along with the kernel




## Android /init

Config file

```
/init.rc
init.hardware.rc
init.usb.rc
init.hardware.usb.rc
```

multiple configurations

```
No run-levels, but offers configuration options
through triggers and system properties
```


Watchdog

```
Services are kept alive by default, unless
defined as oneshot . Services may also further
be defined as critical , which will force the
system to reboot if they cannot be restarted.
```

Adopting orphan processes

```
/init registers a handler for SIGCHLD
which the kernel will automatically send on child
process exit.

```


Socket assignment

```
init can bind a UNIX domain socket for a child, which can then get it through
android_get_control_socket
```

Triggered operation

```
init can execute commands on any
system property change, allowing it to run pre-
defined commands on triggers that can be set
by any (or some) users
```

Handling uevents

```
init also spawns itself as ueventd ,
with separate config files
```


## topics
* [System Properties](systemProperties.md)
* [ueventd]
* [watchdogd]
* [init Config files]
* [init triggers]
* [oneshot]
* [critical]
* [android_get_control_socket]
