9/27/2022
* Process management 
	* Registers
	* Memory management
		* Stack vs Heap
		* Code
* Threads
	* What do threads share with the processes
		* Threads have their own stack but not their own heap, they share this
		* Share address space
		* Threads have their own registers
* What is context switching
	* Switching the context for one process back to another process
	* Time multiplexing


* It's just the reason is you need to have an ability to execute different sections of code at the same time with kernel threads you can't you don't have to just do pseudo parallelism, we call it concurrency, concurrency is a special case. 
* If we have user level threads and one thread tries to divide by 0 it kills the whole process, this is a downside
* Suppose a thread wants to read from a file the whole process has to stop too because the file is shared between all the threads in the file. This is why you need kernel level threads for servers and even driven code for simulation of this 
* There can be multiple readers or 1 writer at a time
* What if one process wants to write, should all the readers get suspendended/put on a queue.
* Threadsafe
	* 2 different threads will be making a pushback, popfront, etc at the same time, and it makes those operations atomic. Which means you can't be interrupted once you start that operation
* Spooling
	* Simultaneous, Peripherals, Online
* Put a gate/sentinel in front of your file that says "busy", this causes more issues because multiple threads can see the file as being "open" to look at and then all of them change the gate to closed
* Avoiding Race Conditions
	* Good Solution must have the following:
		1. No two processes may be simultaneously in their respective critical sections/regions
		2. No assumptions may be made about their speeds or number of CPUs
		3. No process running outside their C.R. may block another process
		4. No process should have to wait forever "starvation"
* Mutual Exclusion
	* Attempts to solutions
	1. Disabling Interrupts
	   ![[Pasted image 20220927111359.png]]
	2. Lock Variable
	      lock variable = 0 
	      enter_region: 
	      lock = 1;
	      C.R. code
	      
	      
	      leave_region: = 0
	      
	      process A sets lock = 1
	      A runs
	      process B sets lock = 1
	      B runs
	      
	      violates the first condition of the avoiding race conditions
	3. Strict Alternation
	   violates rule 3 because they're doing busy waiting. A thread that's not running can block another thread that's also not running
	4. Peterson's Solution	   
*  livelock vs deadlock


9/29/2022
* Busy waiting
	* Continuously testing a variable until some value appears
* Spin Lock
	* If busy waiting is expected to be short for a lock
* Peterson's Solution
	* Must have a enter region and a leave region
	* Show that you're interested in entering critical region
	* Set turn to true or yourself
	* While the turn is the current process and the process is the one that's interested you infinitely loop
	* If the process isn't interested it simply leaves the function.
	* When the process leaves the function, it's interested value getts set to false so it won't go back into the while loop if it reenters the enter_region function
	* Only for 2 processes
* Thread safe
	* All operations/methods within cannot be interrupted while they're in process
	* There is an enter_region and leave_region for all these processes
* Semaphore
	* A datatype, a binary one could 0 or 1
	* A counting one could be all the integer values
* Whenever you have a shared input place, you have a race condition
* 