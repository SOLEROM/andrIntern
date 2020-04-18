# systemServer

* functions as the service host process, wherein most services are implemented as threads


## calling pattern
* Android's framework services are implemented in systemServer threads
* rely on Inter-Process Communication (IPC) in order to invoke
* using the Binder, Android's properietary IPC mechanism
* Applications need to call on the Binder in their own process 
* that will obtain an endpoint descriptor connected to the remote service
* Methods then be invoked through IPC messages, through a pattern known as Remote Procedure Call (RPC)
* get to know [RPC](rpc.md) pattern
