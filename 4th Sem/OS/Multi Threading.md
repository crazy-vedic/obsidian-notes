Many to One model:
	Many user threads are taken care of by a single kernel thread
Many to Many
	Many user threads are taken care of many kernel threads


## Thread Library
	Allows programmer to interact with threading using a system api

Thread cancellation,
	terminating it before it has finished working
		Asynchronous cancellation, it terminates it immidietly
		Deferred cancelllation, allows a target thread to periodically check if it should be cancelled
	