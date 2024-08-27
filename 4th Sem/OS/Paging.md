Paging is storage mechanism to retrieve processes from secondary memory to main memory as pages. 
We are supposed to break each process into individual pages
![[Pasted image 20240404103936.png]] Note: Frame size must be = Page size

	Let Logical be 128 KB, physical 512kb, page size be 16kb
	no of bits in logical/physical=17/19
	no of pages in logical: logical / page size = 8
	no of frames in main: physical / page size = 512/16
	page table size: num of pages * page size=32*16kb

Translation Look-Aside Buffer
![[Pasted image 20240408101942.png]]
Note: TLB is faster and smaller than the main memory but cheaper and bigger than the register.
It allows us to access very frequently accessed pages, quickly, those are stored in TLB

TLB access time=c, tcb hit ratio = x
Effective access time = hit(c+m) +miss*(c+m+m)

c=10, m =80, hit=0.6
effective memory access time = 0.6*(10+80) + 0.4(10+80+80)=122



Page Replacement Algorithm:
FIFO PRA
LRU PRA
Optimal: Looks into the future, the frame which is used the last, that one is replaced
FIFO: First in first out
LRU: Least recently used, slightly similar to optimal but looks in the past
![[Pasted image 20240412103225.png]]

<a href="https://www.javatpoint.com/what-is-hashed-page-table-in-operating-system">Hashed</a>


<a href="https://www.javatpoint.com/os-disk-scheduling">Disk Scheduling</a>
- FCFS scheduling algorithm
- SSTF (shortest seek time first) algorithm
- SCAN scheduling
- C-SCAN scheduling
- LOOK Scheduling
- C-LOOK scheduling

![[Pasted image 20240408104757.png]]

