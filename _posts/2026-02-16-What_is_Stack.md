---
layout: article
title:  The stack 
tags: basics
article_header:
  type: cover
  image:
    src: /images/hacker.png
    
---

### What is the Stack?

It's been a little while since my last post.

In this one I thought it would be good to go over another core concept in low level Programming / analysis.
This is the concepts of the Stack.

The stack is a 64 bit register within the cpu commonly refered to as RSP (Register Stack Pointer.)

It follows a last in first out approach meaning that the last data pushed to the "top" of the stack is going to be the first "popped" from the stack.
The main purpose behind it is to allocate a portion of memory for the main function of a program to allow the temporary storage and retrieval of data.
In terms of memory address, the stack begins at a high address and then grows to lower addresses when more data is pushed onto it, and then back to a high address when data is removed.

This means that as the stack grows it moves towards lower memory addresses. If we use too much of the "stack" we can run into some weird issues.

RSP, points to the top of the stack, meaning that this is the lowest memory address at the time, and when we pop these valeus off the stack it then grows towards a higher memory address again. Data still exists when the stack shrinks however it is considered to not exist/undefined.