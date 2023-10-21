#card/OS/introduction
what is multiprogramming
?
- ==Multiple programs/jobs== reside in the main memory for execution. The operating system selects and executes one of these jobs on to the CPU.
- If the job in execution requires an I/O operation, another job which is ready for execution is scheduled on the CPU.
- increased CPU utilization.
- Increased throughput of the system.


what is multitasking
?
- ==Multi-tasking== is a logical extension of multi-programming systems. The jobs are executed on the CPU in time sharing mode.
- The main advantage of multi-tasking systems is good response time.


Real time operating system::![[Pasted image 20231021220801.png]]


Long-term scheduler::![[Pasted image 20231021221034.png]]


Medium-term scheduler::![[Pasted image 20231021221056.png]]


Short-term scheduler::![[Pasted image 20231021221119.png]]


##### In multithreading, the threads of the same process share, which of the things
?
- user address space, 
- files, 
- signal and 
- signal handlers etc.


##### In multithreading, each thread has its own, which of the things
?
- stack, 
- thread id, 
- CPU state information (control and status registers, stack pointers) and 
- scheduling information (thread state, priority etc.).


User level threads versus kernel level threads::![[Pasted image 20231021221810.png]]