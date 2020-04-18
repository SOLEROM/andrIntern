# RPC pattern

IPC: 

```
Inter Process Communication (IPC) is a blanket term for all forms of
communication between processes. These include various forms of message passing,
but also shared resources (most notably, shared memory), along with synchronization
objects (mutexes and the like), meant to ensure safety in concurrent access to shared
resources (i.e. prevent data corruption which occurs when two writers attempt to
modify the same data item, or race conditions between readers and writers).
```

RPC:

```
Remote Procedure Call (RPC) is a specific term for a method of IPC, which hides the
actual communication inside procedure (method) calls. The client calls a local method,
which in turn is responsible for transparently handling the IPC with the remote server -
which may at times be on a different machine. The method serializes its arguments into
a message, which is then transported to the server's method, where the arguments are
deserialized, acted upon, and the same occurs (in reverse) for passing the return values
of the method, if any.
```

* any RPC mechanism is also an IPC mechanism , but not vice versa
* Android's service calling pattern implements RPC


## Comparison of RPC mechanisms in common operating systems

```
OS 	Mechanism 	Scope 		Directory 	Preprocessor 	Transport
=====	==========	=============	===========	=============	============
UN*X 	SunRPC 		Local/Remote 	portmapper 	rpcgen 		UDP/TCP
Android Binder 		Local 		servicemanager 	aidl 		/dev/binder
```

* scope: denoting whether the RPCs are used in between hosts (remote), or only on the local host
* Directory: The server providing the lookup functionality for locating services
* Preprocessor: The tool used to generate the serialization and deserialization code for messages
* Transport: The medium for message passing
