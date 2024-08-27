Recoverable:
	In a schedule, commit operation should be done in the same order that write is done 

Cascadeless/Cascading:
	Cascading happens during dirty read, when data is used from uncommited T1, and then the T1 is aborted, then the T2 who dirty read also needs to cascade abort

Fail-Stop Assumption:
	Non volatile storage is safe despite system crash

## Log-Based Recovery
`
	Log records are kept on a non volatile, safe secondary storage
	<Ti Start> Log Record
	Write (X) -> <Ti, X, V1, V2> V1 is X BEFORE, V2 is AFTER
	After last log of Ti, <Ti, Commit>

	Deferred recovery:
		Only takes place if a Ti has a START and a Ti commit
		only redo is possible, no undo, so if db crashed, we will redo the valid transaction logs
	Immediate recovery:
		undo and redo is possible, redo is done if commit is found, undo is done if no commit found. 
		undo has priority over redo
		Undo starts moving back from the last log of Ti, undoing all operations one by one
		undo does the opposite of the expected, new value -> old value
		Redo starts forward from the first log of Ti, redoing all of the operations one by one
		Note: *IDEMPOTENT* is important, because all the logs may be executed more than one time by mistake. Idempotent= executing the operations multiple times has the same effect as doing it once
	CheckPoints:
		(if any uncommitted, fuck off and undo, if any committed but not checkpoint, redo)
		During recovery, we only need to find the first Ti with a start, before the checkpoint
		then you only need to consider those logs which take place after that start
		Active transaction:
			those that start before the checkpoint, but haven't committed while checkpoint
		If there is incomplete process, undo it
		If completed process after checkpoint, redo it