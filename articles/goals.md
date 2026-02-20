
***
Let’s build an OS, but wait
===========================


where is the goal post?

![Photo by Alfan Nasihun Amin on Unsplash](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*hqfzzBXLIlyvqUZN)

Engineers had figured out the problem statement and realized that they have to build an operating system that makes their work easier and manages resources. But how? Where to begin?

To build an OS, you first need to define properly what is it that they are building.

Like if you are to construct a bridge, you first define which 2 points that bridge will connect. In short, you define a _goal_ of bridge is to connect city A to city B.

The same way, an operating system is a bridge between hardware and user.

Engineer 1: What are we trying to achieve by creating an OS?

Engineer 2: We are trying to make our and computer work easier, faster, secure, and more manageable by creating an OS.

Engineer 1: Then, what are goals for an OS? Define goals for OS.

Engineer 2: I just said.

Engineer 1: Yes, but that is our goal. Like _our_ goal is to construct a bridge. But the bridge should also have some goals such as be strong and durable in storms and hurricanes, able to withstand 100s of trucks passing by at high speed. Proper lightning to avoid accidents. To help reach commuters from city A to city B.

Engineer 2: I see what you did there. To define goals for OS properly, lets run through again the common tasks of a computer.

One: A student will use a computer, to listen music, edit documents, watch a movie, play games, study, chat. It can also happen that the user is downloading a movie from the internet while listening to a music. There are N number of things that can be done with a computer at any given time.

Goal 1: multitasking. (aka concurrency)

Two: An employee is preparing a report. Suddenly, lights went off. His work is lost. To avoid this frustration, we must persist this data. Although, he can choose to save the file or not, but in case he doesn’t OS should restore the file at a reasonable point at least, without losing all his effort.

Goal 2: persistence.

Three: The student comes back after school and wants to play his favourite game. He opens the game and should sees his last score, the missions all intact. Nothing should get lost. And as he continues to play, his progress should update in real time. But how do we make computer memorize or remember stuff? Like we know we have data storage in hard drive but repeatedly writing and reading into it is slow.

Goal 3: managing memory.

and all this while keeping **protection** and **security** at the forefront. Goal 4 and 5.

Now pause… before we move ahead. I want to write about 3 important components of a computer that makes a computer, complete.

You see, there are 3 main components inside a computer:

1.  CPU or Processor (the brain)
2.  Main Memory or RAM
3.  Disk

Whenever I use the term “memory” throughout the OS — Bits and Bytes, it means RAM. To speak of HDD or Disk, the term is “storage”.

Again, memory is but RAM in the simplest terms. Call it main memory if you can. Every program/app[1] you run uses RAM repeatedly. Memory is accessed all the time throughout the lifecycle of the program. Even the browser I am using right now, the code and instructions for the browser are also in the main memory.

So whenever, you are using a computer, the CPU is repeatedly talking to and from RAM. It stops talking when you shut down the computer or pull the plug.

Now, engineers are closer to defining goals for the OS. The OS should consider these 3 member as its family:

CPU, because obviously.

Main memory (to remember)

and storage device (to persist data long term and not piss off the user if he loses data)

and the goals at this point are kinda hazy [2], but can be written as:

1.  an OS should able to handle and perform multiple task in isolation
2.  an OS should gatekeep programs from touching the hardware directly, hence security and protection of data and resoruces

Next we will know about the reality of these components. The limitations, the constraints. The pitfalls. Because you cannot construct a bridge without knowing how firm the ground is, the soil and sand, what is the speed of water, if that bridge will even survive its own weight or not. What will happen if 1000s of cargo trucks cross through it? How will the bridge survive a strong tornado? What if there is flood? How much water can make the bridge foundation weak enough to collapse?

Knowing limitations and constraints is acknowledging and establishing boundaries. It helps in building better bridge (and OS), durable, long lasting, reliable, safe. Basically, it ensures that our goals are grounded in reality.

**Next we will cover:** Constraints and Limitations

[1] _You will notice that I am using program, application, app, software interchangeably or with slashes. But soon, we will cover the differences and use that which fits the context._

[2] _The goals of an OS is virtualisation, concurrency, persistence. I am not writing virtualisation explicitly. I would rather arrive at that instead of just putting out what the book says._
