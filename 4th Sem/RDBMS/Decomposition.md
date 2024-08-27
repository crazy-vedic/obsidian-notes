Decomposition
While decomposing, 
Union must have all attributes
Intersection must be a key to one or more tables
	Lossless Join Decomposition:
		On Decomposing and joining, if number of tuples is same, it is lossless, perfect
		Break the R into R1, R2, depending on whatever we care about (B, then if B+ = BEF, then R1= BEF). 
		Next then find second part, get a foreign key, all of the dependencies should be included, the intersection is B, then B+ should be R1 or R2, then it is lossless
	Dependency-Preserving Decomposition
		![[Pasted image 20240226105819.png|200]]
		Create a list of Relations, then of all possible non trivial FDs in a table with relations as columns
		Cross out all of those FDs which don't membership test, of the main FD relation set
		Now that makes F', now we check if F' = F or not

R(ABCDEG)
F={AB->C,AC->B,AD->E,B->D,BC->A,E->G}
D={ABC,ACDE,ADG}
(AC)+ = {A,C,B,D,E,G} => ABC, ACDE is lossless
since {A,C,B,D,E,G} and {A,D,G} Membership Test: ka decomposition ka join, is the original set, lossless
{A,C,B,D,E,G} and {A,D,G}
{A,D,G}+ = {A,B,C,D,E,G} means lossless

### Canonical Cover, Minimal Cover
Minimal Cover:
	Here when you have excess, remove the right side of an FD
	Used to remove spurious columns from FD sets
		Case:                                   Minimal                                 Extraneous
		{A**B**->C,A->C}                      {A->C}                                      B
		{A**B**->C,A->B}                      {A->C,A->B}                              B
		{A->B**C**,B->C}                       {A->B,B->C}                             C
		{AB->C**D**,BC->D}                  {AB->C,BC->D}                         D
	Q Find the minimal of {A***B***CD->E,E->D,A->B,AC->D}
		Since ABCD->E and A->B
		so ACD -> E
		Since ACD ->E and AC->D
		So AC -> E

[[Normalization]]
