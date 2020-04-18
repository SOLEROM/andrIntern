# The Framework Service

* native-level processes - implemented in C/C++, has no direct programmatic interface from the Java layer
* thier are services which support the operating system itself
* Applications:
 * make use of services provided by the Dalvik-level frameworks
 * have a Java language interface, 
 * run in the context of one process: system_server
 * are reachable with the help of servicemanager


* [servicemanager](../deamons/servicemanager.md)
	* [service tool](../tools/service.md)
	* [dumpsys tool](../tools/dumpsys.md)


* [systemServer](systemServer.md)
	* [rpc](rpc.md)

* [binder](binder.md) 
	* [bindump](../tools/bindump.md)
