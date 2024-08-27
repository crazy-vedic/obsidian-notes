- [ ] ## Select Operation
	sigma symbol
	1. Notation:  σ p(r)  
	
	**Where:**
	
	**σ** is used for selection prediction  
	**r** is used for relation  n
	**p** is used as a propositional logic formula which may use connectors like: AND OR and NOT. These relational can use as relational operators like =, ≠, ≥, <, >, ≤.

## Project Operation
![[Pasted image 20240124153940.png]]
1. Notation: ∏ A1, A2, An (r)
## Union Operatio[]()n
r U s {t | t belongs r OR t belongs s}
must have same number of attributes

R
(1,1),(1,2),(2,1)
S
(1,2),(2,3)

rUs = (1,1),(1,2),(2,1),(2,3)


## Set Difference
R - S = {t | t belongs R AND t not belongs S}

## Cartesian Product 
R x S = {tq | t belongs r AND q belongs s}
**BOTH R AND S MUST BE DISJOINT TO PERFORM CARTESIAN, ELSE IT IS A NATURAL JOIN**
E x D
E
(1,4)
D
(2,3)
(5,1)

E x D
(1,4,2,3)
(1,4,5,1)

## Rename Operation
	ρ
	RHO Symbol, can rename table or columns
	1. ρ(new, old)


write a relational algebra query to find all loans (Lno) of rs 100+
∏ Lno ( σ amt>100(loan))

find names of all customers having loan at jaipur 
∏ cname (σ borrower.lno == loan.lno AND loan.bname == "Jaipur"  (borrower X loan))

These operations help us simplify the query but they do not add any extra power to the basic 6 operations 
## Intersection Operation ∩

## Join Operation
	Theta and Equi-Join are implemented on cartesian product, equi is only for equal, but theta can take conditions
	Theta Join: Conditional Join
		theta R.B<S.C can be implemented using cartesian product with select as well
	Equi-Join:
		Only one column is checked for equality
		Matching columns will still be implemented: R_no will be (S.R_no, T.R_no)
	Natural Join is R*S
		Multiple columns are checked, all those which have the same name
		If there are any matching columns (R.A and S.A), then only the cartesian product in which R.A == S.a will be outputted
## Division Operation
	Note: S should be subset of R
	r ÷ s =  ΠSid(Entrolled) - ΠSid(ΠSid(Entrolled) X ΠCid(Course) - Enrolled)
	IF ABCD in R and CD in S
	If any of distinct AB values also have ALL OF CD in S,
	then answer contains THOSE DISTINCT AB VALUE (columns of r-columns of s)
## Outer Join
### Left Outer Join ⟕
	All left side columns to be added, if there are missing right side values, then take NULL values in them
### Right Outer Join ⟖

### Full Outer Join ⟗

## Three-Valued Operations, T,F,U
Unknown : N
Any comparison operation with NULL operation generates NULL
U or t = t
U or f = U
U or U = U

U AND T = U
U AND F = F 
U AND U = U

NOT U = U 

## Aggregate Functions:
	SUM,COUNT,MIN,MAX,AVG (ignore NULL values)
	Note: Select(Sigma) operations treat null as false


[[Multi-Valued Dependencies]]

