1) Insertion Anomaly
2) Updation Anomaly
3) Deletion Anomaly

Database Design Goals
	0% Redundancy
	Lossless Join decomposition
	Dependency Preserving Decomposition
Functional Dependency: 
	Single Valued FD -> 1NF,2NF,3NF, BCNF
	Multi- Valued FD -> 4 NF
Let R be a schema, let X, Y be 2 sets in R
if t1, t2 2 tuples in R
-> == "Functionally Determines Y"
then X -> Y 
	This implies that t1.x = t2.y && t1.y = t2.y
	Trivial & Non-Trivial FD
		X->Y is called trivial if Y is subset of X
	Semi Trivial FD => a FD which contains both trivial and non trivial 
	A->A is Reflexive property
	If X ∩ Y is phi, it's non trivial FD