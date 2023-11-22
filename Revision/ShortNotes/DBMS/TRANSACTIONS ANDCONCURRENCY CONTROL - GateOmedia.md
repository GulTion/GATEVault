---
type: ShortNotes
subject: DBMS
sr-due: 2023-11-22
sr-interval: 1
sr-ease: 130
---
#note 

# System Crash
If System crash/failure happen, required operation to recover are
1. All **committed** transaction until previous checkpoint will perform *Redo*.
2. All **uncommitted** transaction in entire system will perform *undo*.
3. *Clean* all log entries.

> [!NOTE] Number of possible serial Schedules `n`
> transactions is `n!`

![[Pasted image 20231120223652.png]]

![[Pasted image 20231120224054.png]]

![[Pasted image 20231120224113.png]]

![[Pasted image 20231120224143.png]]
![[Pasted image 20231120224316.png]]

![[Pasted image 20231120224339.png]]


