* * * * *

### The Origin Story

![](https://cdn-images-1.medium.com/max/1600/0*amOS5DDYuOzbaUiK)

Photo by [Lucas Myers](https://unsplash.com/@unthunk?utm_source=medium&utm_medium=referral) on [Unsplash](https://unsplash.com?utm_source=medium&utm_medium=referral)

In our previous article [What is a computer?](https://medium.com/operating-system-bits-and-pieces/what-is-a-computer-b15bb0359bdd), I mentioned that there was a human operator in the days mainframes to take orders and feed jobs to mainframe computer.

Now it would be tiresome for humans to switch between multiple tasks, manage multiple orders and operations, and make no mistakes. There could be that they might miss some tasks too and businesses don't like that. It's loss of money.

So we needed a system that could handle all these, however simple or complex, tasks faster, in a parallel, reliable, and efficient way.

> Yes, what modern OS does automatically, was done by human operator deciding which program should run next. This mode of computing was known as batch processing. It's like how exam answer sheets are checked. Checker has 5000 answer sheets and he won't check papers one by one. He would pick a batch of, lets say 100 papers from the pile and check those first and continue.

Now, it's not that there were no crucial pieces of software before OS. There were. It's just that it was known as Library. "OS" then, was just a library of commonly used functions. It was limited.

For ex: a library for reading files, writing files. another for doing calculations, another for filtering, some program to find a piece of information from millions of data.

To paint a clear picture, if Kodak company wanted to know which camera models sold highest in which country, that requires a program. And that same program can be used to find the highest-selling camera in various regions for Nikon.

**So what was the problem with libraries?**

It is that libraries had direct control over the resources. Like, a program that can do stuff for Kodak can also *interfere* with Nikon. Or worse Kodak's balance sheet gets overwritten by Nikon balance sheet. Absolute Blunder! No such thing as reverts or backups in 70s. Hardware parts were anyways super expensive.

Programmers also realized that a bad intentioned programmer can access the memory and erase or manipulate data causing chaos for computers and its users.

This is where programmers decided that **Reliability and Protection** must be uncompromising factor in computing systems. Followed by multitasking and speed. But how do they do that? You cannot have people all the time. So you need a system to carry out operations with precision, security and protection in mind, manage resources efficiently and securely.

The problem was not limited to programs having direct access to resources. There was also no way to check or verify if a certain program even needs to access resources in the first place. Like saying, there was no security check or guards to decide what instruction should run and what should not.

* * * * *

**Dumb Question Alert: What has resources or hardware to do with this?**

It's like asking what has bones and flesh to do with living a life. Whatever happens, eventually happen at hardware level. I can see myself writing an article on Hardware and Software someday, but for now, just remember, whatever computing is, it is talking to hardware. You store your pictures in your thumb drive, SSD. Data is stored in memory (RAM) when a program is running, you Facetime your friend and you see each other through camera. and listen via mic. I am typing this sentence using keyboard.

* * * * *

You cannot mess with hardware *directly*. You cannot allow any program to touch that *directly*, either. But you need to use it, right? How do you?

You do it with control. You introduce control.

Now picture this: In a single computer, Kodak company data and Nikon company data , both exist. Now a computer has no thought or judgment of its own by nature. whatever a program instructs, computer shall execute. But how does it know that it has to fetch only Kodak's data and not Nikon.

Sure, operator can specify that as an argument, but the program is still touching the storage area where other company data also exists. It's like sending a clerk to fetch Kodak files from the storage room which is meant to be secure. But he can also fetch Nikon files (unauthorised).

And at first, it's not an ethical problem only.

First, It's a disturbance problem. If you are making sandwich, you want bread and veggies, not baking ingredients closer to you which cause chaos.

Second, it's trust and security concern. Only authorised people and family members should have access to your car keys and fewer can drive when needed.

Third, here it becomes an ethical problem, because we cannot predict someone's intentions. An attacker can run a malicious program to steal data. A thief can pose as amazon delivery guy and pose serious danger.

* * * * *

So, you create a system that controls what program *actually* needs what resources. Like if a program that is being run for Kodak should only have Kodak related data. and the same program if run for Nikon should only work with its own data. All in **Isolation** while a manager supervises and oversees**.**

**Isolation** is keyword. Remember this alongside **reliability**, **multi-tasking**, **security**, **protection**.

So, in order to create a system that is reliable, offers protection, does work in isolation, programmers created something called the operating system.

Operating system as the name suggests, has to do something with *operates* or operations. It operates a system. Like a supervisor. A every efficient manager an OS is. It protects hardware and manages how programs or applications should interact with the hardware.

OS was also known as master control program. [1]

So, an OS is a collection (library) of multiple softwares that does many jobs at once like assigning tasks to a CPU, running applications and programs, remembering data, storing info, etc.

[1] *It is more commonly known as resource manager because it manages resources. Resources being CPU, Ram, hard drives, keyboards, mouse, etc. But how does it do all of that? We will get there, in time, slowly.*
