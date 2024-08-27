Efficiency:
	Completion time: From GANTT CHART
	Turn Around time: Completion - arrival
	Waiting time: How long is process idle (turn around - burst time)
	Response time: (first time process is run) - Arrival
Pre-Emptive: Means can break off the process while it's working (time.sleep(), or I/O protocol)
## First Come First Serve
No matter what, the first process to come is the first to be finished
Non-pre-emptive
![[Pasted image 20240125100605.png]]Burst time is the amount of time required to finish the process
**Convoy Effect** : When a big process is blocking a tiny process

## Shortest Job First
[[Estimation of Burst time]]
P1,3,1
p2,1,4
p3,4,2
p4,0,6
p5,2,3

P4: 0->6
P2: 6->7
P5: 7->9
P1: 9->12
P3: 12->16
Turn around, 9,6,12,6,7
Waiting time: 8,2,10,4,6

## Longest Job First
non pre emptive

## Highest response ratio next 

## Shortest Remaining time first
	ALSO KNOWN AS SJF PRE-EMPTYIVE BECAUSE IT IS DYNAMIC

## Longest Remaining time first
	Also known as LJF PRE EMPTIVE SINCE IT IS DYNAMIC

## Round Robin
	A time quantum is is declared, say 4 ms. if burst period is longer than quantum, then it is pre-empted and context switches to another process, giving each process in the ready queue the same amount of time (ready queue is a circular queue)
	Note: With a lower quantum, more context switches, lower response time
		With a higher quantum, it just becomes FCFS

## Priority Scheduling
	All processes have a certain "priority" assigned to it, depending on whether it is pre-emptive or not, processes will NECESSARILY be executed in priority order

## MultiLevel Queue Scheduling
	Different types of processes can have multiple queues, foreground and background can have different algorithms and can have a priotity of their own
	Only after priority 1 queue is empty, will it move on to priority 2 queue