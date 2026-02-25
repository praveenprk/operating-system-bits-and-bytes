***
The Abstraction: Process
========================

![Photo by Suzanne D. Williams on Unsplash](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*E8pRlFUQgiaTdSfF)

We have covered virtualisation, abstraction, program. It is time to know about the most fundamental abstraction an OS provides: Process. We will also answer how to provide illusions of many CPUs? Because we have limited CPUs and unlimited programs to run.

**Crux of the problem: How to provide virtualisation? How to provide this illusion of many CPUs?**

> OS provides this illusion, first by virtualisation. Second by running one process first, stopping it, then running another process, stopping it , then coming back to the some other process. OS does this so fast, it promotes an illusion that there are many virtual CPUs exist when there are only one or few. This technique is known as time sharing of the CPU. The OS basically **shares time of the CPU** across programs. Time sharing allows users to run as many concurrent processes as they like. It has a cost though: performance. As each will run slowly if the CPU must be shared.

### **But how does it implement virtualisation of CPU?**

To do so, OS needs 2 things:

1.  **Low level mechanisms:** will come to it later. These are some low level methods and protocols.
2.  **High level intelligence:** these are policies in the OS. There are types of policies like scheduling policy which decides what program should run next if the user wants to run 5 programs at a time.

Pay attention now, virtualisation alone cannot run programs. It gives a platform for programs to run within it safely. It is like a container inside which a program runs. Virtualising CPU means creating as many containers as programs. 10 programs, 10 containers. This is where process comes in.

### **What is a Process?**

Process is simply a running program. Programs alone are lifeless. They just reside in the disk waiting to be called into action. It is the OS that takes these programs and gets them running and doing into something useful.

When you double-click on a program to open it, OS transforms that program into a process.

What is a process again? A running program. There is more to it though. It is a set of actions while the program is running. So **what does a process consist of?**

A Process consists of different pieces and parts of the system it interacts with. Parts that will access or affect any of the system components during its lifecycle.

> Lifecycle of a process is defined by how long a program runs. For ex: you open a music player and play 7 songs and close the music player. Considering each song is 5 mins. Lifecycle of its process will be 7 x 5 = 35 mins. This is an oversimplification, of course.

### **What makes up a process? What gives shape to a process?**

To answer this we have to understand its machine state. What a program can read and write when it is running. What hardware is important to the execution of the program? Any program needs memory to run, of course. All the data it reads and writes is in memory. Instructions lie in memory. Thus the memory that the process can use (called its address space) is part of the process.

Also, another part of the process’s machine state is registers. The fastest. Many instructions explicitly read and update registers so they are clearly important to the execution of the process.

Finally, programs often access hard drives to store and retrieve data or files. So, storage device is also another piece of hardware that makes up a process.

**Elements of a Process:**

1.  Memory (Address space)
2.  Registers
3.  Disk

Process API
-----------

All modern OS provides some APIs or interface to work with processes. When you double-click on an app, it calls one of those APIs. When you click on that red x close button, and the app closes, it calls some API. Those APIs are:

1. create(): creates a new process
2. destroy(): kills/quits a running process
3. wait(): waits for some async action to be completed before it can be killed
4. miscellaneous control: such as stop a process for a while and continue it
5. status(): returns process information like how long it has run, what state is in and so on.

### How is a Process created in the first place?

How does a program transforms into process? How does the OS get a program up and running? How does process creation actually work?

The first thing that OS must do is to **LOAD** the program’s code and static data onto memory (address space of the process). You see programs reside on disk in .exe or .app format. So, when you double-click on any app, **the OS loads the code and program data from disk to memory**.

> Now if a program is large, like a photo editor or video editor app, then its code and data will also be large enough. In such case, OS uses lazy loading. This means it doesn’t load all the code and data into memory from Disk at once, but does so as needed during program execution.
> 
> Like, it can load the UI code of the program at once and show, but a certain feature of the program, its code, gets loaded only when the user wants to use it. We will know more about these when we read about virtualisation of memory.

Once the program code and static data are loaded onto memory, OS must do some other things before starting the process. It should **allocate some memory space and assign it to the process for use**. This memory space is called address space.

Why does it assign a memory space? Because the program now turned process needs space to put its code, instructions, data, images, etc.

How does the space look like? It looks like stack and heap.

Stack is a type of memory space, more accurately called as “data structure”[1], where program’s data, functions, params, variables are stored.

Whereas heap is memory place like pile of clothes on chair. This heap is suitable for keeping data structures such as linked lists and trees. Heap is needed for dynamically allocated data.

Heap is small at first, like your chair you have 2–3 clothes at first, over days, heap ends up with 10s of clothes. Similarly, OS also allocates more memory for heap during program runtime as requested.

Then, the OS does some initialisation tasks for I/O related works using file descriptors and things which will read under Persistence topic.

### What makes up a process? How OS turns a program into process?

**OS follows three steps:**
1. Loads the code and static data onto memory
2. Allocate space in virtual memory (address space). Stack for function, params, variables and heap for dynamically allocated data as requested
3. Initialises tasks for I/O related works using file descriptors

**In short:**

1.  OS Loads code and static data
2.  Allocates space memory in virtual memory
3.  Initialises tasks for I/O

### Process States

At any given time, a process can be in any one of the **3 states**:

1.  **Ready** — Process is ready to run but for some reason OS has chosen not to run it. NOT executing instructions yet.
2.  **Running** — process is running on processor and executing instructions
3.  **Blocked** — the process has performed some kind of asynchronous operation which until completed, process is blocked. For ex: until a file is uploaded or until the user clicks on a button

Every process goes through this cycle of **ready > running > blocked > ready > running > blocked**. This is called **state transitions.**

After looking closely, a process can go from ready to running and then running to blocked then again blocked to ready before running, as per OS discretion. OS can move the process across transition as required.

When a process is transitioned from ready and is about to run, it is called the process is **scheduled.**
When a process is transitioned from running to ready, it is called **descheduled**.

You see the OS must take many decisions when running processes and moving it across state transitions. OS here acts like a traffic control system. It runs many processes and all these processes request data from memory, disk, network, or even user, when process0 is blocked, OS gives process1 a chance to run, then process2, when process0 has got the data it needs, OS moves the process0 from blocked to ready, and runs it if OS decides. Decisions whether to run a process or not is made by OS Scheduler which we will cover sometime later.

_[1] Data structure is an interesting and dreaded concept amongst computer science students. It has nothing to do with difficulty level of the topic. The problem is the way data structure is approached and introduced which is often aesthetic and academic rather than practical. You might see some "real-life" examples relating to data structures online but those don't do the justice to the topic. Data structures are one of the core topics of computing. Although it is out of scope of the publication, I will cover what a data structure is, because I find them interesting._
