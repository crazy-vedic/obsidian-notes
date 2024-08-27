L1: Primary cache, fast and small CPU cache
L2: Secondary, larger than L1, may be embedded on the CPU but has a high speed bus connecting the cpu
L3: Specialized memory developed to improve the performance of L1 and L2. This is usually shared between cores. It's faster than DRAM

Continous Memory Management Scheme
	The simplest scheme, mainly divided into two partitions, OS resides in one partition, lowest memory, while user processes is loaded into the other partition
Multiple Partitioning
	Fixed Partitioning:
		All remaining space on the top is divided into fixed size blobs
Compaction:
	Moving all free space to a single combination of all of the space, thus fixing fragmentation.
	Problem: Efficiency is decreased because a lot of memory movement is required, CPU will remain idle for this entire time



Allocation Algorithm
1. First Fit: Searches for the first partition large enough to  fit
2. Next Fit: Same as first but searches AFTER the current node
3. Best Fit: Searches for the minimum fitting partition
4. Worst Fit: Searches for the largest partition
5. Quick Fit: 



Given memory partition of: 100,500,200,300,600kb, how would first fit, best fit, worst fit fill proceesss of 212,417,112,420kb. which algo makes most efficient use of memory?
![[Pasted image 20240404103526.png]]


[[Paging]]
