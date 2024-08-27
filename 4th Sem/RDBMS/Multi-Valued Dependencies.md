Represented by X ->> Y
For single valued:
	t1.x=t2.x implies that t1.y=t2.y

Let t1,t2,t3,t4 be 4 tuples of R, 
1 => t1.x=t2.x=t3.x = t4.x 
2 => t1.y=t2.y=t3.y = t4.y 

T3.(R-Y-X) = T2.(R-Y-X)
t4.y=t2.y
t4.(R-Y-X) = T1.(R-Y-X)

simplify:
Let R be a relational schema, (X,Y) be attribute sets of R, Z = R-XUY
X->>Y exists IFF
1. T1.x=T2.x=T3.x=T4.x 
2. T1.y=T2.y && T3.y=T4.y 
3. T1.z=T3.z && T2.z=T4.z

Applying complement Rule
if X->> Y exists, then
X->>R-{XUY) also should exist

Applying Augmentation Rule, if 
X->>Y
then XZ->WY, where Z superset of W

Applying Transitive Rule, if 
X->>Y and Y->>Z
then here, X->>(Z-Y)

Applying Replication Rule, if
X->Y, then X->>Y also

Note: Union and Decomposition do not apply to MVD