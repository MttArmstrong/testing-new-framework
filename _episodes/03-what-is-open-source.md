---
title: "What is 'Open Source'?"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---

## Learning Objectives

* Understand the role of copyright and licenses in guiding how developers approach contributing to the code and users approach using it.Understand why open-source licenses are popular in scientific software.
* Understand why using existing open-source licenses is preferable to creating new ones.
* Understand what tools are available to help select open-source licenses.
* Understand the necessity and value of clearly documenting the choice of license in your code repository and in the code itself.

## Outline

* The de facto arbiter of whether a license is, in fact, “open source” is the Open Source Initiative (OSI, [https://opensource.org/](https://opensource.org/)).  
    * The Free Software Foundation (FSF) is also influential in open source licensing discussions ([https://www.fsf.org/licensing/](https://www.fsf.org/licensing/)). 
    * Choose an existing OSI-approved license rather than creating a new one.  There are ~80 to choose from that cover most situations.
    * OSI has been reluctant to add to the proliferation of open source licenses by approving new ones.
    * Some publication venues (e.g., Journal of Open Source Software), will only accept OSI-approved licenses.
    * There are tools available to walk you through decision trees to select open source licenses, such as [https://choosealicense.com/](https://choosealicense.com/).  They can be very useful.

## The Licensing Spectrum

Proprietary or Closed Licenses

Free or Open Licenses

All Rights Reserved

**Free vs Open Source?**

* “Free” in licensing discussions should refer strictly to “freedom” (to do certain things with the software)

* Often gets conflated with “free as in beer”, muddling the discussion.  Hence some prefer term “open source”

**Major names in Free/Open Source Software:**

* Free Software Foundation (FSF) [http://fsf.org/licensing](http://fsf.org/licensing)

* Open Source Initiative (OSI) [http://opensource.org](http://opensource.org/)

*Common misconception: Nothing in the definition of free or open source software prevents you from making money from it! (more later)*

## Defining Free Software: The Four Freedoms

*From the Free Software Foundation*

* The freedom to  **run the program** for any purpose
* The freedom to  **study how the program works** , and  **change it**  so it does your computing as you wish
  * **Access to the source code** is a precondition for this
* The freedom to  **redistribute copies** so you can help your neighbor
* The freedom to  **distribute copies of your modified versions** to others.  By doing this you can give the whole community a chance to benefit from your changes
  * **Access to the source code** is a precondition for this

*The OSI has a definition which amounts to the same thing, for most purposes*

## Permissive vs Copyleft OS Licenses

Permissive

* Licensee can distribute derivative works as they see fit
  * Relicensing of derivatives is allowed
  * Including proprietary licenses
* Examples
  * Apache License
  * MIT License
  * BSD License

Copyleft

* Licensee must distribute derivative works as open source
  * Also referred to as “restrictive” or “viral”
* Examples
  * GPL (v2 and v3)
  * LGPL

*Note:* Derived works may be held private and never released

## What is a Derivative Work?

* *A derivative work is an expressive creation that includes major copyright-protected elements of a previously created first work* (Wikipedia)
* Basically: modifications to someone else’s software
* But what about linking to a library? (Statically vs dynamically?) Interacting via pipes?  Use as a component in a coupled multiphysics application?
  * Opinions differ
  * FSF (GPL) considers everything in a single executable to be a derived work (source of “viral” label)
  * LGPL created for libraries – says linking not considered derived work
  * Matters less for permissive licenses
  * Leads to concerns over “compatibility” in combining software under different licenses (more later)

## Test: Is this an Open Source License? (A real-world example)

In order to acquire access to the code sources, the recipient agrees:

1. **to compile/use the XYZZY source code AS IS without modification;** users however are welcome to request changes, or to contribute modifications subject to approval of the authors;

2. **if the copy of the XYZZY downloaded by the authorized user is made available to third parties, to ensure that the user agreement is followed by the third parties;**

3. to send a one-time email to xyzzy@example.com describing planned research using that module

4. prior to publication, to email a draft of the article/letter/note to xyzzy@example.com

5. to include in published results or presentations the proper code name(s) and appropriate references.

## Answer: Is this an Open Source License? No (A real-world example)

In order to acquire access to the code sources, the recipient agrees:

1. **to compile/use the XYZZY source code AS IS without modification;** users however are welcome to request changes, or to contribute modifications subject to approval of the authors;

2. **if the copy of the XYZZY downloaded by the authorized user is made available to third parties, to ensure that the user agreement is followed by the third parties;**

***This violates the freedom of being able to distribute copies of your modified version of the code to others***

*Perhaps they want to impose some measure of “quality control” over modifications?  Maybe they’ve had problems in the past with users distributing modified code with errors that are believed to reflect poorly on the original code?*

*Possible alternative: Some open source licenses include a requirement that derivatives must be clearly distinguished from the original (e.g., different name)*

## Open Licensing of Non-Software Artifacts

* Creative Commons is a family of licenses analogous to open source, but for things other than software
* License variants
  * CC BY (Attribution)
  * CC BY-SA (Attribution-ShareAlike)
  * CC BY-ND (Attribution-NoDerivs)
  * CC BY-NC (Attribution-NonCommercial)
  * CC BY-NC-SA (Attribution-NonCommercial-ShareAlike)
  * CC BY-NC-ND (Attribution-NonCommercial-NoDerivs)
* CC0 Public Domain Dedication
  * Indicates intent to place artifact in the public domain
  * Doesn’t satisfy legal requirements in all jurisdictions
* *See*  *[https://creativecommons.org](https://creativecommons.org/)*

![]({{ page.root }}/fig/licensing3.png)

![]({{ page.root }}/fig/licensing4.png)


{% include links.md %}
