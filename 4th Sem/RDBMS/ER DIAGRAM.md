               https://www.javatpoint.com/dbms-er-model-concept
Double Rectangle:
	Weak Entity ( Can't diffrentiate entities on the basis of this)
Double Diamond(relationship):
	Identifying relationship:
		1. Identified by one strong and one weak attribute
		2. Weak entity must be connected to a strong one with **Double Diamond, and Total Participation.**
Participation:
	Partial Participation: single line
	Total Participation: double line
Relationships:
	Unary relationship:
		Self-refrential
	Binary relationship
Cardinality of relationships:
	1:1
	1:Many
	Many:1
	Many:Many


## Converting ER to a Table
	Create a R, that includes all simple attributes 
	Include all simple component attributes of composite attributes
	choose one of the key attributes as primary key
	if the chosen key is composite, the set of simple attributes that form it, will together form the primary key of R

	For Each weak entity type W, with owner entity E
	Create relation R, and include all simple attributes and simple components of composite attributes of W as attributes of R.
	In addition, include as foreign key, attributes of R the primary key attributes of the relation that correspond to the owner entity types


	For each binary 1:1 relationship
	Identify the relations S and T that coresspond to entity types participating in R. Choose one of these, and include as foreign key, the primary key of the other
	It is better to choose S as a total participation attribute
	Include the simple attributes of the 1:1 as attributes of S
	If both participations are total, can merge both into a single relation
	
	For each 1:N relation
		Identify the S that represents N side
		Include as foreign key in S, the primary key of T

	For each M:N relationship
		Create a new relation S to represent R
		Primary key of both the strong attributes are added, so composite primary key is formed.
		Also, inlcude any simple attributes of the M:N relationship as attributes of S

	For each multi-valued attribute:
		New table is formed
Note: No new relation is formed for 1:1 and 1:N
