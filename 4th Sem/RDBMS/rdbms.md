Books:
	 1. Korth
	 2. Navathe
Suggested	 
	1. Raghuramakrisman
	2. 
Database Design Goals
	0% Redundancy
	Lossless Join decomposition
	Dependency Preserving Decomposition
A table/relation contains rows and columns
rows are also "Records", "Tuples"
columns are "Fields"
Null value is when a value is not known atm

RDBMS better than file management system to maintain consistency, and data integrity
inconsistency can consist of things like redundancy, or lack of atomicity
atomicity: if an operation is initiated, it should be completed in its entirety, or cancelled, no partial operations should take place
concurrency: if multiple users are trying to read/write some data, they should all be serviced in time

databases: set of inter-related data; not just any data
DBMS: Store, Visualize ,Access ,Update data

Domain: Possible values of the data eg: gpa: >0<10
Data Integrity: 

Attributes can be:
	Single Valued: Cannot be broken 
	Multi-Valued
	Simple
	Composite Attribute: something that can be broken into multiple simple parts
	Derived: can be derived from other attributes

Primary Key, Super Key
	An attribute, or multiple which can uniquely identify each tuple in a given relation
	If Primary key is multi-valued, then each attribute is known as prime attribute
Extraneous attribute: 
	The unnecessary attributes of a combination of attributes that form a super key for example in Aadhar + city, city is extraneous and aadhar is the simple super key .
Candidate Key:
	Minimal super key is called candidate key
Alternate Key:
	All candidate keys not primary keys

Q: Let R be a relational schema R(A1->An)
	How many super keys are possible if there is only 1 candidate key?
	We find the power set, or unique combinations of all items except for the candidate key, then add candidate key at the end, so we can have 2^(n-1)
Q How many possible with A1, A2 candidate keys
2^(n-1) is if only a1 is sk, or if a2 is sk  :: 2^(n-1) + 2^(n-1)
but intersection is where a1 AND a2 is present :: -2^(n-2)
Q: If A1A2, A2A3
	then add A1A2+ A2 A3 but remove A1A2A3, so n-2-n-2+n-3

HW Q: A1,A2,A3,


## [[ER DIAGRAM]]


Foreign Key:
	An attribute in the referencing relation, that acts as primary key of the referenced relation
	In the referencing table, foreign key can have null value
[[Relational Algebra]]


[[Axioms]]

On Delete in a parent-child relation
There can be "No Action", "on delete null", "on delete cascade"
In general, on delete cascade is best

[[Decomposition]]

[[Anomalies]]

[[Multi-Valued Dependencies]]

[[Transactions]]

[[Concurrency Control]]

[[Recovery System]]