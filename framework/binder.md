# binder

* The underlying transport for service (and, indeed, all inter-app) communication is Android is the Binder mechanism
* accessible to applications via /dev/binder
* this is elaborately designed IPC framework
* is charged with:
 * dispatching messages
 * passing around objects, descriptors
 * providing reliability and security


* /dev/binder - readily accessible (readable/writable) to all processes.

* Virtually every process in the system (With the exception of a few native processes) opens a handle to /dev/binder
* process is viewed through the /proc/pid/fd directory

* Binder is a Remote Procedure Call mechanism, allowing applications to communicate programmatically, but without having to worry about how to send and receive messages

## what binder do:

### Locating the service process
* In most cases, the client and the service are two different processes
* The Binder needs to locate the service process for the client
* the location service  is technically handled by serviceManager
* but serviceManger is only responsible for maintaing the service directory, mapping an interface name to a Binder handle
* The "handle" is given to the serviceManager by Binder
* only Binder knows the "true" meaning of the underlying PID wherein the service is located

### Delivering the message
* AIDL is used to generate the code which takes the parameters of the called method and serializes or deserializes them
* The passing of the serialized structure from one process to another, however, is handled by Binder itself


### Delivering objects
* Binder can be used to pass around objects like service handles or file descriptors
* allows a trusted process (such as systemServer) to natively open a device or socket for an untrusted process (such as a user app)

### Supporting credentials
* A recipient of a message has to be able to verify the identity of the sender
* Binder is aware of its users' credentials - PID and UID - and securely embeds them in messages


## tools
* see [bindump](../tools/bindump.md)
