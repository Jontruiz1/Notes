8/30/2022

* Layers of Abstraction
* Resource manager
	* Hardware and Software
		* Disk drives
		* Video Cards
		* RAM
* Multiplexing
	* Trying to weave 2 tasks together whether by illusion or truly weaving them together
* Talked about shells here
* Important for operating systems to provide virtualization
	* Parallels or Bootcamp for MacOS
* Timesharing
	* Rather than a card, you could use some kind of tube to sent commands on your behalf


9/1/2022

* Building a CPU?
	* Gotta figure out instructions for it, do we wanna use registers to add numbers together, these kinds of questions
	* Layers at the hardware level
* Machine Organization
	* Instruction Set Architecture
	* Micro-architecture
		* Intel
		* AMD
* Registers
	* High-speed memory units to store temp results and control info
	* Internal to CPU
	  
	* Program Counter
		* Address to the next instruction
	* Instruction Register	  
		* Holds current instruction
	* Stack Pointer
		* Points to the bottom of the runtime stack
	* Base register
		* Points to bottom of active function stack frame
	* Program Status Word
		* Mode bit
			* Kernal mode or user mode
	* User --> Kernel
* Processor
	* Executes instructions
	* Fetch, Decode, Execute
		* Fetch
			* Fetches next instruction from mem into instruction register
			* Change program counter to point to following instruction
		* Decode
			* Determine type of instruction fetched
		* Execute
			* Fetch Operands
			* Operate
			* Store results 
			* If instruction uses a word in memory, determine where it is
* A program is a sequence of machine instructions
* Data-level parallelism 
	* may be used in applications because there are many data items that be operated on at the same time
* Task-level parallelism
	* may be used in applications because the tasks of work are created that can operate independently and largely in true parllelism.
	* We write programs that designate certain tasks to specific parts of the CPU
* Instruction-level parallelism
	* utilized by compilers in limited way using pipelining and predicative branching
* When OS finishes services the request generated bia trap instruction, user program is restarated or completely exited
* Multithreading
* GPU
	* Processor with thousands of tiny cores like graphics rendering
	* Not good at serial tasks like maybe typing a 1000 page paper, you don't know where each page ends 
	* Can be useful for encryption or network traffic
* Memory
	* Registers
		* < 1KB capacity
		* < 1 nanosecond access time
	* Cache
		* Mostly controlled by hardware
		* Divided by cache lines
		* Can convert long path names into a disk address for the SSD or disk where file is located into the cache
		* 4 - 8 MB
		* 1 - 87
	* Main memory
		* 16 - 64 GB
		* 10 - 50
	* HDD / SSD
	* Store capacity goes in powers of 2 but time does not 
	* Volatile
		* Registers, cache, and RAM
	* Non-volatile
		* Magnetic Disks and SSD
		* ROM, EEPROM, Flash, CMOS(technically)



9/6/2022
* Principle of Locality of Reference
	* Temporal
		* Address is likely access several times in short intervals of times
		* If you grab an address from somewhere you're likely to continue accessing that address in the future.
	* Spatial
		* Data are accessed in clusters; they are nearby each other.
	* Sequential
		* Instructions tend to be accessed sequentially
	* Good code will tend to write and read from within the same addresses over and over again
	* Focus on Temporal and Spatial
* 3 ways for I/O
	* Busy Waiting
		* 
	* Interrupt-Driven
		* 
	* Direct Memory Access (DMA) Controller
		* a
* Interrupts
	* Interrupt vector
		* In RAM
	* Save context of current process context registers
	* PC loaded with interrupt vector index i
		* interrupt j
		* Starting address

9/8/22
* Operating System types
	* Mainframe
	* Server
	* Personal Computer
	* Smartphone and Handheld
	* Internet of Things and Embedded
		* Embedded not connected to outside things but needs to exist to control various appliances
	* Real Time
		* Need to react to certain things
	* Smart Card
		* Card-sized devices containing a CPU
* Processes
	* Address Space
		* Vector/Array of bytes
	* How would you define a process

9/13/2022
* Files
* RWX bits
	* Read, Write, Execute
	* chmod u + w
		* Add write privilege to the user
	* chmod u - w
		* Take away write privilege from the user
* Shell
	* Main interface between user and operating system
	* POSIX Compliant
		* Wrote shell according to POSIX rule
	* When a command is typed in Shell, it creates a process