LockX:
	Exclusive Lock, it acquires lock for both read and write protocol
LockS:
	Shared lock, it acquires lock only for reading, allowing other T to lockS as well
![[Pasted image 20240408111702.png]]

WW problem:
	Lost update
	![[Pasted image 20240506000726.png]]

WR problem:
	Dirty Read 
	![[Pasted image 20240506000658.png]]

RW problem:
	Violation of Isolation![[Pasted image 20240506000534.png]]

# IMPORTANT

2 Phase Locking Protocol
	Guarantee: conflict serializable, but deadlock and cascading rollback
	**Growing phase:** In the growing phase, a new lock on the data item may be acquired by the transaction, but none can be released.
	**Shrinking phase:** In the shrinking phase, existing lock held by the transaction may be released, but no new locks can be acquired.
	Between these two phases, there is "Lock Point"

Strict 2 phase locking
	Guarantee: cascadeless rollback
	Transaction must hold all of its **X** locks until it has finished
	Shrinking: S locks are unlocked

Rigorous 2 phase 
	Guarantee: Serialized in the order they commit
	**X AND S** Locks are held until commit abort
	Shinking: doesn't exist


|                     | Conflict Serializable | View Serializable | Recoverable | Cascadeless | Deadlock Free |
| ------------------- | --------------------- | ----------------- | ----------- | ----------- | ------------- |
| Time stamp ordering | YES                   | YES               | NO          | NO          | YES           |
| Thomas Write Rule   | NO                    | YES               | NO          | NO          | YES           |
| 2 PL                | YES                   | YES               | NO          | NO          | NO            |
| Rigorous 2PL        | YES                   | YES               | YES         | YES         | NO            |
| Strict 2PL          | YES                   | YES               | YES         | YES         | NO            |
|                     |                       |                   |             |             |               |



# IN PPT FROM HERE TILL DEADLOCK, NOT COMING (exclusive)


## Deadlock prevention stratagies
1. Wait-Die Non-Pre-Emptive:
	Older transaction may wait for younger ones to release data items.
	Younger never waits for old one, they are rolled back instead
	A transaction may die several times before acquiring lock
2. Wound-wait Pre-emptive:
	Older transaction wounds (force rollback) of younger transaction, instead of waiting for them.
	Younger may wait for older ones
	May be fewer rollback than wait-die


### other than above, only thomas write is imp

[[Recovery System]]
