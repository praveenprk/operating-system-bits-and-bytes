***
Breaking Reality
================

![Photo by Anirudh on Unsplash](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*RRAZNogiNg9SGZCi)

We know that an OS is a very efficient manager. That means a good OS should able to perform multiple jobs at once. A good manager makes reasonable decisions too. So, a good OS should decide which program to run, what resources to allocate to a program, what not to run and so many more? In short, OS should be able to run programs at its own discretion. When you want to run a program, the OS does some bookkeeping and decides to run it or not.

Before designing a working operating system, engineers knew they had one CPU which should run hundreds of programs and limited memory should remember relevant information about the running program.

But again, how do you get the OS to run multiple programs on one CPU?

How do you get the OS to manage a RAM that remembers thousands of information?

Idea: Think dorm room. You program the OS to treat your resources like a dorm room where each program has a bunk bed and memory block. In this way, the program can now share CPU and memory.

But what happens to security and protection? If program A is using CPU and program B is also using it, A can interfere or block B or B can break and steal data from A.

Yes, that can totally happen. But we need to share resources for optimisation, proper utilisation of the resources (CPU & memory). So we design the OS to prevent attacks in someway and share resources safely.

Hmm, safely.

How do we design OS to share resource safely, not compromising on security?

By sharing smartly and carefully. Managed sharing of resources, you can call it. We design OS to share resources safely and smartly.

Okay, so how to share resources “smartly and safely”?

Answer: Illusion.

Magic.

What?

Yes. That is the solution: create an illusion.

That’s not real!

That’s the point, it doesn’t need to be real. In fact, the apps you use are not real. but they work, right? As if they are not real form wise, you cannot hold the apps in your hand, but they function, just like real.

Then how does the program run on something that is not real? Like they need CPU and memory to run. How does this happen? This is so interesting and so confusing.

Yes, the real CPU and memory are there. It’s just that we **provide an illusion for the program** that they are using the real CPU. But instead they will use the illusion of the CPU.

I will write it again, to give you a different perspective.

When you want a CPU to run many programs, the OS should create an illusion or a safe environment for each program. And each program uses the illusion of CPU instead of the real one. The program doesn’t know that it is working with an illusion. Just like you don’t know what happens when you type google.com in your browser and press enter. Yet you end up on Google.

This creation of illusion is called virtualisation [1]. When OS creates an illusion, it’s called virtualisation. OS virtualises the CPU, it virtualises the RAM.

That is the first goal of an OS: Virtualisation.

Now each program is **contained** within its virtual environment. Within their own created illusion. Each program is safe. Their data and code safe, for now.

**Now let’s see what is happening roughly step by step:**

1.  You want to run 100 programs, you open 100 programs
2.  The OS takes this open instructions, one by one, very fast, and knows that it has to create virtual CPUs and RAMs for 100 programs [2]
3.  The OS spawns illusions or virtual resources for each program as required, one by one, super fast
4.  OS assigns each virtual environments to 100 programs
5.  Those programs now think they have the resources to themselves and they run happily in their own safe virtual environments without complaining.

Now a natural question should arise in your mind: What is this “virtual”, virtualisation, virtual reality, virtual this, virtual that? We will take that in the next one.

[1] Like everything in computing Virtualisation is a huge and dense topic. I will try to dedicate a good amount of section for the same. I am as excited about this._

[2] Everything in computing happens sequentially, but at high speed. There is something known as context switch responsible for this. We will cover the nitty-gritty of how this happens over the course of the publication._
