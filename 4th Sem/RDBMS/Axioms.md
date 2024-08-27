## Armstrongs' Axioms
Reflexivity: similar to triviality:
	if B subset of A then A->B
Transitive Axiom
	A->B, B->C
	then A->C
	Pseudo-Transitivity: 
		If A->B & WB->C
		then WA -> C
Augmentation Rule
	A->B
	AY->BY
	AX -> B also
	Pseudo-Augmentation:
		?
Union Rule
	X->Y, X->Z
	X->YZ
Decomposition
	X->YZ
	X->Y,X->Z
Closure Set:
X+ Represents all attributes that can be functionally defined by X
For example:
	FD {A->B, B->C, C->D}
	A+ = (A,B,C,D)
	B+ = (B,C,D)
	C+ = (C,D)
	D+ = (D)
	AB+ = A+ U B+

AB->CD, AF -> D, DE -> F, C -> G, F -> E, G -> A
CF+ -> {C,F,G,E,A,D}
BG+ -> {B,G,A,C,D}
AF+ -> {A,F,D,E}
AB+ -> (A,B,C,D,G)

TIP: IF THE PRIME ATTRIBUTE CAN BE FOUND IN THE RIGHT SIDE OF FD IN THE FD LIST, THEN THERE CAN BE MORE THAN ONE CANDIDATE KEY, LOOK AT QUESTION BELOW

Q Find the Candidate key in R(ABCDE),  {AB->C, C->D, B->EA}
	AB+ -> {A,B,C,D,E}
	A+ -> {A}
	B+ -> {B,E,A,C,D}
	HERE, WE LOOK FOR (AB) IN THE RIGHT SIDE, SEE A AND THINK MULTIPLE CANDIDATE, BUT THATS WRONG BECAUSE WE NEED TO LOOK FOR THE PRIME ATTRIBUTE, NOT JUST ANYTHING IN THE SUPER KEY, SO B IS THE ONLY PRIME ATTRIBUTE AND CANDIDATE KEY

Q: R(ABCDE), {AB->C, C->D, D->E,B->A,C->B}
	AB+ = {A,B,C,D,E}
	A+ = {A}
	B+ = {B,A,C,D,E}
	C+ = {C,B,D,E,A}

Q R(ABCDE) , {A->BCDE, BC->ADE,D->E}
A+ = {A,B,C,D,E}
BC+ = {B,C,A,D,E}
B+ = {B}
C+ = {C}


Membership Test
	F: {AB->C, B->D, DE->F, E->G}
	find whether B->C?
		Procedure is finding closure ( B+ ) of the left side, and if C is in that or not 

Functional Dependancy Set Closure
	Set of all functional dependencies, that can be determined by a functional dependency set
	Note: The number of functional dependencies due to and attribute A = (2^n), n is no. of elements in closure of A
	EG: A+:{X,Y,Z}
	then the total dependencies are:
		(phi,X,Y,Z,XY,YZ,ZX,XYZ)
		-
	Q: R(ABC), F: {A->B,B->C}
	Taking 0 attributes, phi+ = {phi}
	Taking 1 attribute, A+ = {A,B,C}, B+ = {B,C}, C+ = {C}
	Taking 2 Attributes {AB}+ = {A,B,C}, {BC}+ = {B,C}, {AC}+ = {A,B,C}
	Taking 3 attributes {ABC}+ = {A,B,C}
	(1)+(8+4+2)+(8+4+8)+(8) = 43
-
	Q: R(AB), F: {A->B, B->C}
			Taking 0 attributes, phi+ = {phi}
		Taking 1 attribute A+ = {A,B}, B+ = {A,B}
		Taking 2 attributes {AB}+ = {A,B}


Equality between 2 F.D. Sets
	"F covers G" 
	Check that all FD sets within G exist within F
	Take FD from G, and compare against closure against F
-
	Q: F: {AB->CD,B->C,C->D}
	  G:   {AB->C,AB->D,C->D}
	F=G?
	F covers G:
		AB -> C Belongs to F?
		{AB}+ -> {A,B,C,D}  YES
		AB-> D belongs to F?
		{AB}+ -> {A,B,C,D}  YES
		C->D Belongs to F?
		C+ = {C,D} YES
	G covers F:
	AB->CD belongs to G?
	{AB}+ = {A,B,C,D} YES
	B->C belongs to G?
	B+ = {B,D} NO
-
	Q F: {A->C,AC->D,E->AD,E->H}
	   G: {A->CD,E_>AH}
	   G covers F:
		   A->C?YES
		   AC->D? YES
		   E->AD? YES
		   E->H?YES
	F covers G:
		A->CD? YES
		E->AH? YES

[[Decomposition]]