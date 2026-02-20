***

Constraints and Limitations
===========================


![Photo by Andrey Volk on Unsplash](https://miro.medium.com/v2/resize:fit:1400/format:webp/0*ET9lKnXjncVlnYoE)

In this section, we will see the reality of these components. The limitations, the constraints. The pitfalls. Because you cannot construct a bridge without knowing how firm the ground is, the soil and sand texture, the speed of water flowing, if that bridge will even survive its own weight. What will happen if 1000s of cargo trucks cross through it? How will the bridge survive a strong tornado? How much water can make the bridge foundation weak enough to collapse?

Knowing limitations and constraints is acknowledging and establishing boundaries. It helps in building better bridge (and OS), durable, long lasting, reliable, safe. Because it forces you to think of all the measures you can take to reduce incidents. Find a work around the constraints, what are right set of trade-offs. Once you know these before designing OS, we can design for reality.

**What are constraints in computing?**
--------------------------------------

Before we answer this, we need to list what are _resources_ in computing.

Resources for building a bridge can be concrete, sand, iron, steel, engineers, masons, cranes. For a computer, resources are CPU/processor, Main memory, Hard drive. These are the primary resources without which a computer is not really a computer. Now, you see resources are limited. Coal, water, trees, time are limited. Renewable or not is not the question. Limited or unlimited is the key point we are talking. “Unlimited” water in the ocean can be desalinised to drink and we end up deserting our planet after 1000s of years; it will eventually reach zero. Same way, CPU is limited because it is made of silicon which comes from earth’s crust. Same goes for RAM. Hard drives are made of magnetic tapes and mechanical parts which are made of steel and copper, also which are limited resources.

**So realise, We have limited resources!**

We have one CPU, a few RAMs, one HDD.

## What hits the limit and when?

The capacity of the resource decides to hit the limit when there is an overflow. If you continue filling a one litre bottle with water, it will overflow eventually.

You see there is one bus which has the capacity of 50 passengers, but the number of travellers at bus stop will always be more than 50. That is multiple buses runs throughout the clock to serve and accomodate more and more passengers. So, the solution here becomes, 5–7 buses everyday throughout the clock, to and fro locations A and B.

**Limited CPU or processing power**

Similarly, a modern computer can handle 500 tasks _at once[1]_. It cannot process 5000 tasks at once. CPU needs to wait for the other tasks to get completed. Also, it won’t wait forever, so many tasks get dropped and never run. Just like many buses, you need to have many CPUs, but it’s impractical, it’s expensive.

You can share one CPU across multiple tasks/programs. But that would be a security concern. And each app requires its own CPU and memory. Meaning, each app should run in **isolation.** Just like an office employee needs their own cubicle to work, every app need its own isolated space to run.

> **Human Limits**
> 
> We wish we had 6 hands, some superpower or magic to get things done. But that’s not the reality. A human can’t sing and read at the same time. You may cook and sing at the same time, but one of those task require more focus than the other. When you are driving, you may sing a song or listen, but you have to keep your senses active around road and surroundings. You don’t do multiple things at once, you do it concurrently. You drive fast fully focused and slow down a bit then sing or smoke to relax. You switch something in your brain actually. This is called context switching which we cover later.

**Limited Main memory or RAM**

Main Memory is second crucial computing resource. Also known as RAM, is accessed frequently non stop by every app that you use. And like CPU, every app need its own memory. Like every employee needs their own desk and drawer. But we have only one or two hardware memory. Here also we can share, but security!

**Limited Storage**

Classic example of limited storage is basement or store room. You can have a large enough store room, but the amount of stuff you have in your home is just not enough most of the times. You need space to store stuff that you can use it when needed. You need space to store old toys or stuff.

**Money**
---------

In early computing days memory and storage devices were super expensive. For perspective, 64 bits of RAM in 1970 cost almost $100. So, this was another main constraint that forced engineers to design around this cost constraint.

I hope I have covered constraints and limitations clearly. Before we dive d into operating system, I needed to paint a picture of what limits and constraints look like in general and connect it to computing resource.

[1] _“at once” is misleading in computing. Nothing happens at once. No two programs run together at once. You play music and browse the web at once, sure. But that is not the computer actually does. If something in computer is happening at once, it is an_ **_illusion. C_**_reating this illusion is the primary goal of operating system. It creates the illusion that there are many CPUs and memory and apps use that illusion to run. This is what I am arriving at._
