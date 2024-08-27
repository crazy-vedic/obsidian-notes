Due to Single Valued FDs
	1,2,3,BCNF, Boyce-Codd 
MTE SYLLABUS TILL BCNF
Due to Multi Valued FDs
	4NF
[[Multi-Valued Dependencies]]

1nf:
	Every attribute must be atomic
	If there exists proper candidate key, then it is 1nf
	Meaning **NO MULTI-VALUED ATTRIBUTE**

2nf:
	Partial FD, if x is reduced, and it is still a functional dependency
	There shouldn't be any prime attribute that determines a non-prime attribute
	Every attribute must be: in a candidate key, or depend fully on a EVERY candidate key
		Does not allow any partial dependency
		Every non-prime attribute is fully functionally dependent on every candidate key 
	This means that if AB is candidate key, AND AB->C THEN A->C OR B->C is not allowed

3nf:
	for all X->Y
	1. Either X is Super Key
	2. Or Y is a prime attribute.

BCNF:
	for all X->Y
	X is super key

4NF:
	R is in BCNF
	If x->>y, then only trivial MVDs should exist
	![[Pasted image 20240502185843.png]]
	left only single MVD should exist, or trivial


![[Pasted image 20240401105506.png]]