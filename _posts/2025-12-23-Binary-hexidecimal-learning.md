---
layout: article
title: Hexidecimal - Binary Conversions and assembly / analysis 
tags: basics
article_header:
  type: cover
  image:
    src: /screenshot.jpg      
---

I'm taking this Journey from a very step by step from the ground up way. So for the past day or so I've been attempting to reinforce certain knowledge that's been lost to me due to lack of practice.

Today I'm re-developing my binary-hexidicmal-decimal conversions.

I've gotten the way to convert hex numbers to decimal down quite easily, though since my mental maths is not the strongest i'm using a calculator.

From my understanding you simply multiply the digits rightmost digit by 1, then every digit to the left of rightmost digit by digit x 16 to the power of however leftmost it is, for example:

0x1337
You multiply:
* 7 x 1
* 3 x 16
* 3 x 16^2
* 1 x 16^3

and vice versa.
The answer being - 4'919

Due to Holidays and studying times, this is just going to be a very compressed long form article that's very relaxed.
Just been trying to get my head around signedness as wel as negative numbers.

### Two's Compliment
This is the process that computers represent signed integers allowing simple binary addition to work for both.
One's compliment is where we inverse the bit's of any binary number to attempt to get it's negative value, however this leaves us with a problem when it comes to adding and subtracting multiple binary numbers.

For example if we have:  

0101  5   
      +  
1010  - 5  
___  
1111 - F which is not correct, we would be expecting the answer to be zero

This is where Two's compliment comes in.
After Taking our flipped bits we simply add 1.

This makes   
0101  5  
     +  
1011 -5  
___  
0000  

Meaning we get the correct answer. 

