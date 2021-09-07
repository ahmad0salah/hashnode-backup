## 7 Essential Tips for Debugging


> “If debugging is the process of removing software bugs, then programming must be the process of putting them in.”

## There will always be BUGS!

Bugs are part of writing software. Be it a new piece of code you're adding or an old module you are fixing. Bugs will be there.
Working with bugs is challenging, both mentally and emotionally. Therefore we need a systematic approach to solving bugs as staring at your screen shouting - "it should be working! Why this is not working" will not resolve anything.


## Be aware of the emotional toll

Most developers suffer from imposter syndrome and not feeling they belong. Especially people who are just starting.
When you get stuck, it's necessary to calm down, be mindful of how you feel and trust the process, and go through a step by step.

*Reminder raise your hand and ask for help when you need it, even if you are a senior engineer. It is OK!*

## The Process

## 1. Reproduce the problem consistently

The first to solve a problem is to define it.
It doesn't make much sense to work on a solution for an ill-defined problem.
Don't think about the code and dedicate all your energy to finding a repeatable step to reproduce this bug.

## 2. Finding the root cause

Now, you got the steps to reproduce the bug. You will have to reduce the steps required to reproduce the bug. This step is critical to isolate the root cause of the problem.

*Don't overload your short-term memory. always write down the steps & even take screenshots/casts if necessary.*

## 3. Now we examine the code

After writing down the minimum steps required to reproduce the bug, you can examine the code.
Your focus should be on isolating the part responsible for this bug. 
Start by finding the module then, the class then, the method where things deviate from the expected behavior.

it's always a good idea to ask a teammate where to start

## 4. The debugger is your friend

print statements are fine. But, the debugger is a powerful tool use it to your advantage.
The debugger allows you to set multiple breakpoints, step in function, display all local variables, and more.

Make sure to know your IDE shortcuts and how to get the most out of it. this will save a lot of time

## 5. Zoom out

Avoid introducing new bugs with your fix.
It's necessary to get an overview of how this area of the code base works.
Identify the moving parts and how they interact. 
What is the business logic and the expected?
Don't make assumptions about the code there is plenty of sneaky edge cases and workarounds everywhere be very wary of brushing off these details.

## 6. Small changes only

Tiny changes are easier to validate wasting, 20 minutes typing and think you've solved it. There is a possibility that you've done too much work or broke something along the way.
Writing long patches will most likely end up with you debugging the newly added code.
and remember, version control is your friend you, can do as many commits as you and eventually squash and tidy up your branch

## 7. Tunnel vision

Sometimes, you have spent too much time with a bug that you can't see what is wrong and all you need is a fresh set of eyes. Ask a teammate or take a 5 min walk.
It's important to recognize this and avoid sinking more time being stuck. 
A great tip to avoid this is to timebox your bugs to a set number of hours, then you must ask for help.