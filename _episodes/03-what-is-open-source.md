---
title: "What is Open Source?"
teaching: 0
exercises: 0
questions:
- "Key question (FIXME)"
objectives:
- "First learning objective. (FIXME)"
keypoints:
- "First key point. Brief Answer to questions. (FIXME)"
---

## Outline

* The de facto arbiter of whether a license is, in fact, “open source” is the Open Source Initiative (OSI, [https://opensource.org/](https://opensource.org/)).  
    * The Free Software Foundation (FSF) is also influential in open source licensing discussions ([https://www.fsf.org/licensing/](https://www.fsf.org/licensing/)). 


Open source is a popular choice in scientific research, for reasons we'll explore in the next episode.
But before that, let's take a deeper look at what we mean by "open source" and some nuances in the spectrum of open-source software licenses.

## The major names in open source

When it comes to defining open-source or free software, there are two major organizations to be aware of.
The [Free Software Foundation](https://fsf.org) (FSF) was founded in 1985 by Richard Stallman.
In addition to advocacy for free software [licensing](http://fsf.org/licensing), the FSF also maintains a sizable number of software products, including GNU Emacs and many of the packages at the core of the GNU/Linux operating system.  
The [Open Source Initiative](http://opensource.org/) (OSI) was founded in 1998 by Eric Raymond and Bruce Perens.
The primary mission of the OSI is to assess licenses and maintain a list of those which they judge to qualify as "open source."
They also engage in advocacy related to open source software.

## "Free" vs "open source"

It may not be surprising, given their names, that the Free Software Foundation tends to use the term "free software", whereas the Open Source Initiative prefers "open source."
Although the FSF uses the term "free" in licensing discussions to refer to the freedom to do certain things with the software, the term often gets conflated with "free" as in no cost, which quickly muddles the discussion.  Hence, some prefer to use the term "open source" for clarity.  You may also see the term "libre" (Spanish for "free") used in place of or together with "free" (i.e., "free/libre") in the context of software.

This lesson generally uses the term "open source."

## Defining free software: The four freedoms

The FSF has a concise [definition of free software](https://www.gnu.org/philosophy/free-sw.en.html#four-freedoms) that revolves around the freedom to do certain things with the software:

0. The freedom to **run the program** for any purpose.
1. The freedom to **study how the program works**, and **change it** so it does your computing as you wish.
2. The freedom to **redistribute copies** so you can help your neighbor.
3. The freedom to **distribute copies of your modified versions** to others.  By doing this you can give the whole community a chance to benefit from your changes.

Note that **access to the source code** is a precondition for freedoms 1 and 3.

The OSI has a [definition of open source](https://opensource.org/osd/) software which is longer, but amounts to the same thing for most purposes.
The OSI definition includes two requirements that are implicit in the FSF freedom 0, but which are worth noting:

* No discrimination against persons or groups, and
* No discrimination against fields of endeavor.

## Permissive vs copyleft open-source licenses

One of the most important distinctions in the spectrum of open-source software licenses is whether they are considered "copyleft" (also called "restrictive") or "permissive."
These terms have to do with how the license treats derivative works (which we'll define more thoroughly in a few moments).

A permissive license allows the licensee to distribute derivative works as they see fit.
This includes the possibility of relicensing the derivative work under another license, possibly even a proprietary license.
Examples of permissive licenses include the [Apache License](https://opensource.org/license/apache-2-0/), the [BSD License](https://opensource.org/license/bsd-3-clause/), and the [MIT License(https://opensource.org/license/mit/).

Copyleft licenses, on the other hand, require that the licensee distribute derivative works under the same license as the original work.
The FSF is one of the main proponents of copyleft licenses, and they created two of the most widely used examples: the [GNU General Public License](https://opensource.org/license/gpl-3-0/) (GPL) and the [GNU Lesser General Public License](https://opensource.org/license/lgpl-3-0/) (LGPL).

## What is a derivative work?

Wikipedia tells us that *a [derivative work](https://en.wikipedia.org/wiki/Derivative_work) is an expressive creation that includes major copyright-protected elements of a previously created first work.*
For software, this amounts to modifications to someone else's software.
So derivative works are extremely common, especially in collaborative software development.

But what about linking to a library?
(And does it matter whether the linkage is static or dynamic?) 
Or software that interacts via pipes?  
Or software that is used as a component in a coupled multiphyscs application?
Are these also modifications to someone else's software?
Opinions differ on such questions.
The Free Software Foundation's GPL license considers everything in a single executable to be a derived work.
(The GPL is sometimes referred to as a "viral" license because it "infects" everything that "touches" it.)
The key difference between the GPL and the LGPL is that the latter says that linking is *not* considered a derivative work.
The FSF refers to the GPL as "strong copyleft"  or "strongly protective" (of software freedom) and the LGPL as a weakened version.
The definition of derivative work matters less for permissive licenses because they are not so rigidly tied to the license of the original work.

But because of these different approaches to dealing with derivative works, concerns about the "compatibility" of licenses may arise when you are combining software under different licenses.
A later episode will explore this in greater detail, but for now, the easiest way to avoid problems with license compatibility is to avoid *distributing* other works with yours.
In other words, don't ship someone else's software package as part of yours.
(Some may consider it a convenience to bundle together all of the dependencies required to build a software package.)
Let the end user put them together (i.e., build the executable that combines them).

This is because of an important fact about open source licenses, even strong copyleft licenses: you're not required to distribute a derived work!
The requirement is that *if* you do distribute it, you do so in conformance with the terms of the license of the original work.
So you can make changes to a piece of software and you're not required to share the derived work with anyone else.
And you can finesse license compatibility issues by letting the end user put everything together rather than you shipping the combined work.

> ## Activity: Is this an open source license?
>
> The following is a real-world example of a software license (lightly obfuscated to protect the identity of the software).  Read it and decide whether it qualifies as "open source."
> 
> In order to acquire access to the code sources, the recipient agrees:
> 
> 1. to compile/use the XYZZY source code AS IS without modification; users however are welcome to request changes, or to contribute modifications subject to approval of the authors;
>
> 2. if the copy of the XYZZY downloaded by the authorized user is made available to third parties, to ensure that the user agreement is followed by the third parties;**
>
> 3. to send a one-time email to xyzzy@example.com describing planned research using that module
>
> 4. prior to publication, to email a draft of the article/letter/note to xyzzy@example.com
>
> 5. to include in published results or presentations the proper code name(s) and appropriate references.
> 
> *Hint: focus on the first two clauses.*
>
> > ## Solution
> > No.  Clauses 1 (especially) and 2 violate the freedom of being able to modify the code and the freedom to distribute copies of your modified version of the code to others.
> > 
> > Why might someone have felt clauses like these were necessary to include in their software license?  Perhaps they've had problems in the past with users distributing modified code with errors that they felt reflected poorly on the original code.  Or perhaps they want to impose some measure of quality control over modifications.
> > 
> > A possible alternative solution would be to include a requirement that derivatives must be clearly distinguished from the original (e.g., different name).  Some open source licenses include such clauses.
>{: .solution}
{: .challenge}

## Open licensing of non-software artifacts

OSI approves open-source licenses for *software.*
But there are many other creative works related to software (or not) that we might want to treat in a similar manner (like documentation for your software, or this lesson).
The [Creative Commons](https://creativecommons.org/) (CC) is a family of licenses analogous to open-source, but for things other than software.
Variants of the Creative Commons license allow you to impose various restrictions, similar to choosing different licenses for software:

  * CC BY (Attribution)
  * CC BY-SA (Attribution-ShareAlike)
  * CC BY-ND (Attribution-NoDerivs)
  * CC BY-NC (Attribution-NonCommercial)
  * CC BY-NC-SA (Attribution-NonCommercial-ShareAlike)
  * CC BY-NC-ND (Attribution-NonCommercial-NoDerivs)

The Attribution clause, which is part of all CC licenses, requires that the user include the appropriate attribution (title, author, source, license) when the work is used.
The ShareAlike clause requires that adaptations (derivatives) be shared under the same terms as the original (analogous to copyleft).
The NoDerives clause says that no derivatives of the work are permitted.
The NonCommercial clause says that only non-commercial uses of the work are permitted.
Without this clause, commercial uses are allowed.

The Creative Commons has developed a set of [badges](https://creativecommons.org/about/downloads#badges) and [icons](https://creativecommons.org/about/downloads#icons) that provide quick visual indicators of the chosen license.
For example, this lesson is licensed under CC BY 4.0:
![CC BY badge]({{ page.root }}/fig/cc-by.png){: width=50%}

There is also a "CC0 Public Domain Dedication" which can be used to indicate intent to place the artifact in the public domain.
However this does not satisfy the legal requirements in all jurisdictions, so if you're serious about placing a work in the public domain, you might want to investigate further.

{% include links.md %}
