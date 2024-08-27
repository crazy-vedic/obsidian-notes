15-20 Marks of Scheduling Algorithms in MTE & ETE
Os is the most important software that runs on a computer, manages all memory and core processes. / Interface b/w user and hardware

Kernel is the active part of os, that is running at all times

Hardware: Basic computing resources
Operating system: controls the use of hardware among various applications

Uses of OS:
	1. Process Management
	   All requests by the user are converted to "process" in the cpu, a process needs resources such as CPU time, memory. Do not let cpu remain idle.
	2. Process synchronization
	3. memory management
	   RAM, a large repository of quickly accessible data shared by CPU and I/O, OS is used to keep track of what memory is used by who
	4. File Management: OS is responsible for file CRUD, mapping to secondary storage
	5. I/O System management
		   Buffer caching, drivers for specific hardware devices

On starting computer, while loading screen is there, "Boot Program" is loaded from main C:\ into the RAM, bringing the actual os into play

Multi-Programming: all jobs are in the ram, whenever cpu is chilling, i/o or something else, then cpu is temporarily assigned another job, throughput is maximum because cpu is never idle
Multi-Tasking, Pre-Emptive: All P1->P4 are given T/4 amount of time
Context switching required, state for all P1->P4 is saved, main memory high req

In multi-processing, parallel computing. There are more than one processsers in the system. this will increase the throughput of the entire system. 
Advantages:
	inc reliability, inc throughput
Disadvantage:
	More sophisticated and complex to avoid processor idle time

Network OS:
	Network traffic reduces due to division between client and the server, this is less expensive to setup.
	However, the failure of the server node will affect the entire system
Real Time Operating System:
	Each job carries a certain deadline in which a job is supposed to executed, medical, weapons
		Hard RTOS: System crashes if deadline not reached
		Soft RTOS: Results are still stored if deadline not reached
		Firm RTOS: Result is ignored and job is done once again
Distributed Operating System:
	All devices in the network are given a specialized responsibility
User application is connected to the system hardware via the system call interface, before which it is in user mode, then after it is in "Kernel Mode" 
System Call is a request from the user software to the kernel

fp = fopen("data.txt","w");
fprintf(fp,data)

[[Scheduling Algorithm]]
[[Estimation of Burst time]]

[[Process Creation]]

[[Inter Process Communications]]
[[Multi Threading]]
[[System Calls]]

[[Memory Management]]
[[Paging]]
