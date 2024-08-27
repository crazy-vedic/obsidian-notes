Number of child process creation is dependent on level of multi-programming
Fork Command, system call, used to create the child process
Dependent on OS:
	Resources received by the child is a subset of the resources received by the parent process
	Every child process may be given extra resources
Note: fork() in c, only creates a child process that runs the code below the fork() that initiated the process itself.
Fork 
	returns P_ID in the parent process
	returns 0 in the child process
	returns negative if fork failed
exec() replaces the current process with another executable
exit() terminates the program with an exit status
wait() 
	the parent uses this to suspend execution until child terminates, using this the exit status of child can be gained
	can be passed an address to int, in which it will store the exit status of the first child that exits
init(): Any orphaned process will be immediately adopted by the special init system process with PID 1.ses execute concurrently
Note: If parent process terminates before the child process, then the children is called "Orphan", and a init() system call is made to create a new temporary process, which gains access to all of the orphans (adopted)
Opposite, if child process is terminated while parent is still running, it's still consuming resources despite being finished. called *ZOMBIE*

