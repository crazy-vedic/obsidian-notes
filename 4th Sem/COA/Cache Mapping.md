Direct Mapping:
![[Pasted image 20240124150342.png]]
	Main Memory:
		first 4 binary digits holds the block number
		last 2 binary digits holds the offset number
		eg: address for 54 is: 110110 : 1101 => Block-13, 10 offset
	Cache Memory
		Cache Line
		Block Offset


Assuming a memory of 2^32, divided into blocks of size 32 bytes, assume a direct mapping cache having 512 cache lines is used, how big is the tag field in bits


# FULL ASSOCIATIVE MAPPING
	Solution to direct mapping => conflict miss problem
	Here any block can be assigned to any cache line, (many to many relationship)
	increases hit latency and cost
	Block Number (Tags) + Block offset(Line Offset)
