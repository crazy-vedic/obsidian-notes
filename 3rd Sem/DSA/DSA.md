Continuous data structure: 
	Has memory allocation all together in the ram

Discontinuous data structure:
	Memory allocation is all over the place


malloc(size)
```c
int* myptr = (int*)malloc(10*sizeof(int));
```
Receives the starting void ptr of an allocated number of bits, like here we requested space for 10 ints in memory
So the following `10*4=40` bits in memory are ours to do anything we want to do with it. conversion is necessary because initially a void ptr is returned to us from malloc

```c
free(myptr);
```
frees up the memory artificially so that other programs can make use of it

```c
int prevList[] = {1,2,3};

//NOW THERE IS AN ARRAY NAMED TEMP WITH 4 SIZE, CONTAINING THE PREVLIST
int *temp = realloc(prevList,4*sizeof(int));
free(prevList)
```

