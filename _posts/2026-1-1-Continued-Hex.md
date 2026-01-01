---
layout: article
title:  Continued Fluency With Hex and manipulating values
tags: basics
article_header:
  type: cover
  image:
    src: /screenshot.jpg      
---

### Hex addition and subtraction.
 
 The course I'm following has suggested becoming more fluent in mental maths in terms of manipuilating hex numbers.
It's relatively simple overall when it comes to addition and multiplication.

 You just have to remember that for any number over 15 since hexadecimal is base 16 there is no representation of that digit.
So what you have to do is divide the number by 16 and then use the remainder as the base then carry the 1 over.

 Simply put if you had.
Hex 24
 it would be represented as:   
 9  
 With the 1 Carried over to the next digit.


 Now where does this come in with subtraction and addition?

 0x967f  +
 0X126B

 Let's break this down step by step.

 We have F-15 + B - 11 
 This would give us 26.
 26 is not able to be represented in hex so we have to do the process listed above.
 26/16 gives us 1.6 so.
 We represent this as A
 then carry the 1.

 this makes 0x968

 our first character for the answer being A
 8 + 6 = 14, so D

 0XDA so far  

 6 + 2 = 8. 
 0X8DA

 9 + 1 = 10 SO a  

 The final answer we get being 

 0XA8DA.

For larger numbers it's best to bring a calculator in, however i'm going to make a python script for this just for the practice.  

Here is the script:  

[My Script](https://github.com/Onekamm/Milkyway/tree/a98829fcc30d88886316640d0779fedff41a1dfc/scripts)


It allows the taking of user input to supply any hexadecimal or well any integer to be fair I haven't bothered handling invalid characters past a certain point.

And calculates the result taking into account the maximum 64 bit register length.


Thank you for reading.