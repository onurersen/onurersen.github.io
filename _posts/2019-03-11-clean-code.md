---
layout: page
title: "Clean Code"
author: "Berat Onur Ersen"
date: 2019-03-11
draft: false
permalink: /2019-03-11-clean-code/
tags: coding
---

In an agile mindset, writing code using best practice approaches is not an easy thing to do. 
If we have time-constraint (we say that we are agile), it becomes a double-edged sword. 
We have to keep it quick and keep doing in ideal form. That is not possible, generally.

![picture alt](/img/clean-code/coding_hell.gif)

Being part of different projects, searching, reading, applying, working with different people approaching issues in different aspects...
all of these bring a developer to a point to analyze what to look for while aiming a best practice implementation.

There evolves the craftsmanship. Raising the quality bar requires hard work, systematic approach, and patience.

Years ago I remember checking on "all-the-time must read" books like Code Complete, Clean Code etc.

... and recently, I made my mind on going through those books carefully with an interiorizing mindset.

So I started with Clean Code by Robert C. Martin. The book starts with mentioning Japanese **5S philosophy** in software craftsmanship.

They are short, clear and very meaningful for a developer:

**Seiri (sort)**

> knowing where things are - using approaches such as *suitable naming*

**Seiton (systematize)**

> a piece of code should be where you expect to find it. - if not *refactor* to get it there.

**Seiso (shine)**

> keep the workspace free of hanging wires, grease, scraps, and waste. *get rid of* traces, unnecessary production artifacts.

**Seiketsu (standardization)**

> having a consistent coding style and set of practices - obeying *standards and conventions*.

**Shutsuke (self-discipline)**

> having the discipline to *follow the practices*, reflect on work and be open for change

![picture alt](/img/clean-code/samurai.gif)

---

I liked this book very much, which made me add those anectodes i came across with.

**Update : 2019_03_15:**  
"Clean code is _focused._ **Each** function, **each** class, **each** module **exposes a single-minded attitude** that remains entirely undistracted, 
and unpolluted, the surrounding details."

**Update : 2019_03_18:**  
"Reduced **duplication**, high **expressiveness**, and early building of **simple abstractions**. That's what makes clean code for me." - Ron Jeffries

**Update : 2019_03_20:**  
"Noise words are another meaningless distinction. Imagine that you have a _Product_ class. If you have another called _ProductInfo_ or _ProductData_, 
you have made the names different without making them mean anything different. _Info_ and _Data_ are indistinct noise words."

**Update : 2019_03_21:**  
"The word _variable_ should never appear in a variable name. The word _table_ should never appear in a table name. Imagine finding one class named _Customer_ and another named _CustomerObject_. What should you understand as the distinction? Which one will represent the best path to a customer's payment history?"

**Update : 2019_03_23:**  
"Classes and objects should have noun or noun phrase names like _Customer_,_WikiPage_,_Account_ and _AddressParser_. Avoid words like <del>Manager</del>, <del>Processor</del>, <del>Data</del> or <del>Info</del> in the name of a class. **A class name should not be a verb.**"

**Update : 2019_03_24:**  
"The name **AccountVisitor** means a great deal to a programmer who is familiar with the VISITOR pattern. What programmer would not know what a **JobQueue** was?"

**Update : 2019_03_25:**  
"**Ideal number of arguments for a function is zero (niladic)**. Next comes one (monadic), followed closely by two (dyadic). Three arguments (triadic) _should be avoided where possible_. More than three (polyadic)" 
requires very special justtification - and shouldn't be used anyway."

**Update : 2019_03_26:**  
"Passing a boolean into a function is a truly terrible practice. It immediately compicates the signature of the method, loudly proclaiming that this function does more than one thing. **It does one thing 
if the flag is true and another if the flag is false!**"

**Update : 2019_03_26:**  
"Structured programming, Aspect Oriented programming, Component Oriented Programming, are all, in part, strategies for eliminating duplication. It would appeat that since the invention of subroutine,
 innovations in software development have been an ongoing attempt to eliminate duplication from our source code."
 
**Update : 2019_03_27:**  
"If you decide to write a comment, then spend the time necessary to make sure it is the best comment you can write. Any comment that forces you to look in another module for the meaning of that comment has failed to communicate to you and is not worth the bits it consumes."

