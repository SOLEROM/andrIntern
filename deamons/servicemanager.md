# servicemanager

* key component of Android's IPC mechanism
* function as a service mapper
* serves as the locator, or directory, for all other operating system services
* key services are dependent on it, and must be restarted with it if it crashes
* designated as critical, which means that init will agressively attempt to restart it, or boot to recovery if it fails to do so


* If any application or system component needs to use another service, it must first consult servicemanager to obtain a handle


* The IPC model of Android provided by a dedicated kernel component - the Binder
* User-mode services access the binder for IPC via a character device node - /dev/binder

## operation:

* call to binder_open obtains the /dev/binder descriptor,
* call to binder_become_context_manager establishes its position
* enters an endless elnless_binder_loop , which blocks on the descriptor, until a transaction (i.e. request from a client) occurs
* the wakes process calls its svcmgr_handler callback, which processes the transaction


* servicemanager should be globally accessible, so that services can register with it, and clients can look them
* services and clients alike can call on defaultServiceManager() - to get a handle to the service manager
* there is no API to remove the service. Services are automatically removed when their proceeses die, because Binder can detect that, and send a death notification.
*


## related tools
* [service](../tools/service.md) 
* [dumpsys](../tools/dumpsys.md)
