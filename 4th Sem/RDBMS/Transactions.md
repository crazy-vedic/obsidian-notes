ACID Property:
Atomicity: All transactions should either complete or should rollback
Consistency: 
1. Total before T occurs = 600+300=900  
2. Total after T occurs= 500+400=900
Isolation: - It shows that the data which is used at the time of execution of a transaction cannot be used by the second transaction until the first one is completed.
Durability: - The durability property is used to indicate the performance of the database's consistent state. It states that the transaction made the permanent changes.

Transaction States:
![[Pasted image 20240401111617.png]]

Active: Instructions being run
Partially Committed: Final instruction have been run, but data has not been stored to the DB
Committed: If all instructions executed and data has been re - stored
Failed: If any of the ACID checks made by the dbms fails, then the dbms makes sure it moves back to its previous consistent state
Aborted: If any of the checks are irrecoverable, then the transaction is aborted, then it can either:
	Re-attempt transaction
	Kill the transaction


## Schedule:
``
	Serial Schedule:
		All transactions take place one by one, synchronously
	Non-Serial Schedule:
		Some transactions may execute concurrently, inter-weaving is allowed. 
	Serializable Schedule:
		A Non-Serial Schedule which has the same output as if the transactions occured serially

CONFLICT SERIALIZABLE:
	Run through time for each instruction, does there exist a conflicting instruction in any of the other transactions? if so, set i->j
**IF THERE IS NO LOOP, MEANS SERIALIZABLE, IF LOOP, UNSURE TRY VIEW**
Precedence Graph:  Perform topological sorting on a precedence graph to find the serialized schedule Topological sorting is done by finding in edge with 0 in degree, then that's your first, remove all connecting edges, repeat

View Equivalent:
	Initial Read: The initial read of both schedule must be the same
	Updated Read: In schedule S1, if Ti is reading A which is updated by Tj then in S2 also, Ti should read A which is updated by Tj.
	Final Write: Final write of both views must be the same

Cascading Rollback:
	![[Pasted image 20240404112534.png]]Here the commit is not done after the Ti write, so a cascading rollback must be performed

Cascadeless Rollback:
	![[Pasted image 20240404112610.png]]
	This is stricter, here we enforce committing after every write

[[Concurrency Control]]
