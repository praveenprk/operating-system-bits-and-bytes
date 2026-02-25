***
What is a Program?
==================

and what happens when a program runs?

So far, you have noticed that I am using programs, apps, software, interchangeably. But at an abstract level, they are different.

In previous articles, I said things like you **run a program**. you **run an application**. A **program or app needs a CPU to run.**

Most of it is true at a surface level. But as you zoom in, you will see they are different.

**What is the difference between program and app?**

Program is the smallest unit of an app. Smallest unit of any software.

App is what happens when multiple programs come together to serve a function.

Take this calculator app for example [1].

![captionless image](https://miro.medium.com/v2/resize:fit:880/format:webp/1*Zj2F55RnYP-QNd8u3m_wAg.png)

Each button corresponds to a tiny program. And then, a calcutor app is a collection of many such tiny programs. Those small programs come together to form an app called calculator to do maths.

When I pressed 9, the program printed 9 on the screen. If I press 8, the same program will print 8. But when I press button C, another program will erase everything.

Now let’s go deeper.

Think of it as multiple type of programs.

In the above calculator app, numbers 0 to 9 are taken under one type of program, let’s call it “Number Program”.

The operators %, X, — , +, = come under “operator program”.

C button comes under “Clear program”.

So how does these programs come together and work like an app.

**Step by step breakdown (assuming you are adding 9 and 8):**

Step 1: You press **9**, the number program prints **9** on screen.

Step 2: Press **+,** the operator program prints **+** on screen.

Step 3: You press 8, the same number program from step 1 prints 8.

Step 4: Now when you press **=,** the operator program sees that and decides you want to see the calculated result. It knows that you typed **+** in step 2, so it sums the numbers provided by Step 1 and 2 and displays the final result.

Step 5: After the calculation is done, you press **C,** the clear program clears the screen so you can continue with next calculation.

It should be clear that how many small or big programs come together to form a big application or software. Each program should be reasonable.

Now we will see the simplest program of all. A program that adds two numbers. This should give you an idea of what a program looks like.

```
let a, b, sum;
sum = a + b;
```

The above program adds two numbers **a** and **b** and stores the result in **sum**. a, b, and sum are called variables. Variables are crucial in any programming language [2] and in any program.

Programs are nothing but instructions. The line “let a, b, sum;” is one instruction. sum = a + b is another instruction. A program is just a bunch of instructions waiting to do as instructed.

**What will happen when you run the above program?**

When you run a program, **CPU executes** those **instructions**. When we run the above example:

CPU executes the line “let a, b, sum;”. This instructs the CPU to declare three variables namely a, b, sum.

Then it executes the second line “sum = a+b;”. This instructs to place in sum the result of a + b.

That’s all you need to know for now. [3]

From now on I will try to use the word **program** at least everywhere**.** But if you find my using app or software, know that I am referring to a program or set of instructions.

_[1] A calculator example because, doing maths was the first motivation behind computers. We built computers to do difficult, large maths. So it is only intuitive that maths is something computers are good at. But there’s a catch. Computers don’t peform maths like we do. Because we have 10 fingers to count so we think in Base10 but computers do everything in 0s and 1s, they think in Base2. They understand well what +, — , X means. They have their own way of doing maths which is covered in Boolean Algebra. That is out of scope for this publication._

_[2] There are many programming languages available. The example program code I wrote is in javascript. The book actually contain examples in C programming language. I am using Javascript because that’s what I write for a living. But I will write only those section of program that will make sense in any language. If something requires advance concepts, then I must write it in C or Nodejs which requires fundamental understanding of at least one programming language._

_[3] OS does a lot of things when you run a program. Before CPU can start executing instructions, OS does some bookkeeping operations using an abstraction called_ **_Process._** _What is a process? We will cover next._
