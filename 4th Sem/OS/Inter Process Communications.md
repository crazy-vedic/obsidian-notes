Pipes
Allows two processes to communicate
`pipe(fd) where fd is just a int fd[2]`
Here after piping, you can fork, then.
**FD[0] is READ FD[1] IS WRITE**
You can initiate it before the fork call

