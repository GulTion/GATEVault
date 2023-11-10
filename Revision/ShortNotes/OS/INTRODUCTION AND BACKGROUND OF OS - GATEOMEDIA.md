---
type: ShortNotes
subject: OS
---
#note
#card/OS/introduction
what is multiprogramming
?
- ==Multiple programs/jobs== reside in the main memory for execution. The operating system selects and executes one of these jobs on to the CPU.
- If the job in execution requires an I/O operation, another job which is ready for execution is scheduled on the CPU.
- increased CPU utilization.
- Increased throughput of the system. <!--SR:!2023-11-16,17,290-->


what is multitasking
?
- ==Multi-tasking== is a logical extension of multi-programming systems. The jobs are executed on the CPU in time sharing mode.
- The main advantage of multi-tasking systems is good response time. <!--SR:!2023-11-15,4,250-->


Real time operating system::![[Pasted image 20231021220801.png]] <!--SR:!2023-12-12,31,270-->


Long-term scheduler::![[Pasted image 20231021221034.png]] <!--SR:!2023-11-15,16,290-->


Medium-term scheduler::![[Pasted image 20231021221056.png]] <!--SR:!2023-12-06,25,270-->


Short-term scheduler::![[Pasted image 20231021221119.png]] <!--SR:!2023-11-14,15,290-->


##### In multithreading, the threads of the same process share, which of the things
?
- user address space,
- files,
- signal and
- signal handlers etc. <!--SR:!2023-11-16,5,250-->


##### In multithreading, each thread has its own, which of the things
?
- stack,
- thread id,
- CPU state information (control and status registers, stack pointers) and
- scheduling information (thread state, priority etc.). <!--SR:!2023-11-12,13,270-->


User level threads versus kernel level threads::![[Pasted image 20231021221810.png]] <!--SR:!2023-11-13,14,290-->