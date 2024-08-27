# CREATING GATES FROM NANDS

SR Latch
[[Flip Flop]]

Register is a small and temporary storage unit inside of the CPU

[[Cache Mapping]]

Cache Memories:
	Block Placement:
		Finding a good place to place the blocks.
		Direct Mapping -> Block No mod Cache lines
		Set Associative mapping
	Block Identification
		Direct -> Find potential match using CL and offset Bits, compare tag
		Associative -> Find potential match using tag
		Set Associative
	Block Replacement:
		When processer replaces an old block in cache, by the new block from main memory
		To be done when cache is full, or when match can't be found
		Very simple in direct mapping, difficult in associative mapping
		For Direct, all memory blocks have a CL specified, so no decision making required
		For Associative, can be placed anywhere in cache
		For Set-Associative can be placed anywhere in the set
			Thus for the above 2, Cache replacement policies are required
		Cache Replacement Policy:
			FIFO: Blocks are replaced from from cache in the order of arrival
	Write Strategy:
		Looking for a data word to modify, in cache
		Write hit -> when data is present in cache
			Write through -> Cache and main memory updated same time, longer times
			Write Back -> Only cache is updated in real time, and uses dirty bit, main update when replacement takes place
		Write Miss -> When data is missing from the cache
				Write Allocation -> Data is brought into the cache, then updated
			No-Write Allocation -> 
Types of cache miss:
	Compulsory Miss: When cache is partially full or when the cache is empty
	Capacity Miss: When cache is full, replacement needed

Implement a cache with FIFO CRP,
	2,3,4,7,6,3,4,7,5,4,7,8

	![[Pasted image 20240201094522.png|200]]
	Find the miss & hit ratio
	For 12 attempts, 7 were a miss, 
		Miss: = 7/12
Implement a cache with LIFO CRP,
	4 lines
	2,3,4,7,6,3,4,7,5,4,7,8
	![[Pasted image 20240201095256.png]]
Implement a cache with MRU CRP,
	Most recently block is replaced, works well with cyclic
	![[Pasted image 20240201095306.png]]

Implement a cache with LRU CRP,
	Here we make a list of the CL,s along with some number of Age bits, for each the age bits are going to be -1'ed, other than the one currently used, that will be maxed out in the bits

LFU Least Frequently Used
	Same as LRU, except frequency bit is stored, not age bit


[[Types of instruction]]

[[Micro-Programmable control units]]

[[Pipelining]]
[[IO]]
