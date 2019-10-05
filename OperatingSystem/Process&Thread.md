## Process
### What is?
> In simple words a process is executing a program. But not all, it’s only an instance of a computing program. Several processes may be associated with the same program. Process contains program code and its current activity.
- 실행 중인 프로그램
- 비동기적 행위
- 실행 중인 프로시저
- 실행 중인 프로시전의 제어 추적
- 운영체제에 들어있는 프로세스 제어 블록
- 프로세서에 할당하여 실행할 수 있는 개체 디스패치가 가능한 대상
## Thread
### what is?
> We can say thread is a light weight process. A thread of execution is the smallest sequence of programmed instructions that can be managed independently by scheduler. Threads reside inside the process. Each thread belongs to exactly one process. No thread exists outside the process.
## Comparison
|Number | Process           | Thread |
|:-----:|:-------------:|:-----:|
|1| System calls involved in process. | No system calls involved.|
|2| Context switching required. | No context switching required..|
|1| Different process have different copies of code and data. | Sharing same copy of code and data can be possible among different threads..|
|1| Operating system treats different process differently. |   All user level threads treated as single task for operating system.|
|1| If a process got blocked, remaining process continue their work. | If a user level thread got blocked, all other threads get blocked since they are treated as single task to OS. (Noted: This is can be avoided in kernel level threads). |
|1| Processes are independent. | Threads exist as subsets of a process. They are dependent. |
|1|   Process run in separate memory space.| Threads run in shared memory space. And use memory of process which it belong to. |
|1|  Processes have their own program counter (PC), register set, and stack space. | Threads share Code section, data section, Address space with other threads. |
|1| Communication between processes requires some time. | Communication between processes requires less time than processes. |
|1| Processes don’t share the memory with any other process. | Threads share the memory with other threads of the same process|
|1| Process have overhead.. | Threads have no overhead. |
> Threads are used for small tasks, whereas processes are used for more ‘heavyweight’ tasks – basically the execution of applications. Another difference between thread and process is that threads within the same process share the same address space, whereas different processes do not.

