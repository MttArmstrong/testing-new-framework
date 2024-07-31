---
title: "Collaboration and Licensing"
teaching: 17
exercises: 15
questions:
- "What are the concerns with accepting code from collaborators?"
- "What mechanisms are there to ensure collaborators agree to license terms?"
- "What concerns are there with using code from online forums?"
- "Why are LLMs challenging for copyright and licensing?"
objectives:
- "Understand the challenges surrounding code contributed from outside the project."
keypoints:
- "Collaborators may be restricted in their ability to contribute to open source projects (e.g. industrial partners) or unable to copyright their work (government employees)."
- "You can include a Contributor License Agreement (CLA) to ensure collaborators agree to license terms prior to committing code."
- "Stackoverflow content is licensed as CC BY-SA, which is incompatible with permissive or proprietary licenses."
- "License and copyright around LLM-generated content is actively being litigated."
---

If you are lucky, you have an open-source project with an active user base and
a few developers to help field issues.  As a project grows, it's possible you
will get pull requests from people you've never met.  Even if the code looks great,
it's possible the has author inadvertently has caused a licensing issue.

A somewhat related topic is how to handle code snippets from external sources
like web forums or large language models.

## Contributors and Licenses

There are two cases where a contributor can cause problems with licensing your code.

First, if you have a copyleft license, contributors from industry may be reluctant
to contribute over fear of accidentally violating the terms of the GPL license.
Since GPL requires derivative works to be copyleft, if the contributor were to
incorporate some of the code into a larger project, they would be obligated to
release the entire code base under the license terms.

Alternatively, if you have a restrictive license, it's possible a contribution may not be
subject to copyright at all!  Any work from a government employee, say a researcher at a
federal agency, is not subject to copyright and is in public domain.

It is important to communicate your license terms to all collaborators and decide
on a license early in a project's life cycle.  Changing a license is possible,
but may require the explicit approval of all contributors; for larger, older
projects the prospect is daunting.

Part of being proactive is developing and publishing your `CONTRIBUTING` guidelines.
You can also choose to use a **Contributor License Agreement** (CLA), which is a legal
document that new contributors must sign prior to merging their code.  While
protective of the software project, CLAs may limit inclusivity by acting as
a barrier to first-time contributors.  They can also create a power imbalance between
maintainers and contributors.  Practically, CLAs often require review and
approval by the legal department of the contributor.

A **Developer Certificate of Origin** (DCO) is a lighter-weight agreement that allows
contributors to confirm the code they commit is suitable for the project license.
They can be integrated into a pull request or commit message instead of a separate legal document.
In either case, the policies for contributors should be clear and easy to find
and verify if legal issues do arise.

> ## Activity
>
> What are the contributor guidelines for some open source code you use?
>
> Pick one dependency or utility you regularly use.
> Does the project have a CONTRIBUTING file? CLA? DCO?  Does the license
> mention contributors?
{: .challenge}

## Code from Internet Forums

Question and answer forums like Stack Overflow provide a valuable avenue for
developers to connect with knowledgeable users covering a range of topics from
installation, language usage, and debugging.  It is satisfying to find the exact
answer to your problem so you can get back to work.  But as with anything else
you see on the internet, the material is subject to copyright.  It is worth
thinking about how you can incorporate solutions found online into your work
while respecting their copyrights.  Material on Stack Overflow, for example,
is published under a CC-BY-SA license ([Creative Commons Attribution Sharealike](https://creativecommons.org/licenses/by-sa/4.0/)).

Generally, if you're using the Stack Overflow material as guidance or documentation,
and adapting it to your particular situation without using text (code) verbatim from the
Stack Overflow posting, it should be relatively straightforward because
you're not making direct use of the copyrighted material. You don't have to disclose where the original
idea came from, but for your own benefit it is a good idea to include the URL
in a comment.  Its also nice to give credit where credit is due.
An example of this kind of use might be if you are searching for how to plot a scatter plot with transparency given by
another column in your dataframe.  An answer may suggest matplotlib, seaborn,
or another plotting library. It may provide example code or command line instructions to make such a plot.
But you adapt it, with your variables and filenames, and other details.  And in the end,
there's probably little from the original post appearing in your code -- maybe routine or command
names and a few key options.

On the other hand, if you are searching for, say, a binary search written in python,
or the answer contains a function snippet for performing the task you need?
Fair use does not use length as a factor, if you directly copy and paste code
and you want to distribute that code, it would then fall under the license applicable to the forum posting.
As mentioned, for Stack Overflow, for example, that's CC-BY-SA.

> ## Pop Quiz
>
> If you use CC-BY-SA work in your project, what kind of license should you use?
>
> > ## Solution
> > Though they are considered appropriate for software *documentation*, the Creative Commons recommend against using their licenses for software per se (see [Can I apply a Creative Commons license to software?](https://creativecommons.org/faq/#can-i-apply-a-creative-commons-license-to-software)). But they do define a concept of "compatibility" between
some CC licenses and software licenses precisely for situations like this (see [Compatible Licenses](https://creativecommons.org/share-your-work/licensing-considerations/compatible-licenses/)).  According to this page, CC-BY-SA 4.0 (not prior versions) is compatible with the [Free Art License](http://artlibre.org/licence/lal/en/) or the [GPLv3](https://www.gnu.org/copyleft/gpl.html) licenses.
>{: .solution}
{: .challenge}

## Generative AI, Large Language Models, and Code Assistants

A recent development for software engineers is the rise of large language models (LLMs)
capable of producing code from English descriptions.  The utilities are integrated
in many search engines, integrated development environments (IDEs), or as standalone assistants.  While performance
and utility can vary wildly, LLMs can increase developer productivity by removing
some of the tedious jobs.  Just be wary, correct-seeming code can be worse than
something clearly wrong!

Just as the technological limits of LLMs are still being discovered, the legal
aspect of AI, copyright, and licensing are actively being determined in court.  There are three
phases where licensing and copyright concerns appear in utilizing LLMs:

1. Does the training process respect the licenses of the code used for training?
2. If you want to refine an LLM, what license is the model distributed with?
3. If I use code generated by an LLM, what attribution does it need and will it affect
my license?

### Ingested Code

Unless you are training your own LLM, this is more of an interesting case study
in copyright than a day-to-day concern.  Since the implementation details of
many LLMs are proprietary, you may not know what code a model was trained on,
what license the code used, or if permission was attained to use the software
for training.

Legal challenges against AI companies have been brought up by artists and
authors, who allege the generation of verbatim passages or replication of
artistic style indicates that the training data included copyrighted material against
the creators' wishes.  Code generation hasn't been included in these lawsuits
so far, but rulings on other domains could affect how LLMs are trained.  If you
are concerned about the origin of code used to train an LLM, look for LLMs that
provide information on the training set and use a training set aligned with your
license and values.

### Refining an LLM

In a technical sense, refining a published network is fairly straight forward!  Just like any other
piece of software, you can follow the license distributed with the material in
creating new works derived from the original network.  However, the weights of
the foundation model could "contain" copyrighted material from data
on which they were trained.  It's possible that during refinement, the network
will retain the copyright material in a form that can be recovered.  Litigation
will be needed to sort out fair use, but keep in mind that refined networks
may contain the foundation model largely unchanged.

### Using Code from LLMs

You may have already used code from an LLM, either to play with a new technology
or even in production to save time on development.  Continuing with the theme
of this section, we don't know all the answers until legislation and lawsuits
settle.

Consider the following scenario: you use an LLM to generate a function that is
later discovered to be verbatim from a copyrighted code base, violating the
license.  Who's liable for damages?  You? The company that trained the network?
The company you pay to use the LLM?  Legally, we don't yet have answers to this,
but getting the code from an LLM may not be considered a defense against the fact
that your code infringes on someone else's copyright.

Some tools have been developed to scan LLM output to flag large snippets that
are present in other sources. Many tech companies don't allow code generation
from outside products due to privacy concerns, as well as licensing issues.
As an aside, if you're interested in a job in industry, you might want to
make sure your coding skills are solid *without* help from an LLM.

The US government recently declared that AI-generated work can not be
copyrighted if it's produced without human intervention beyond prompt engineering.
This is likely to apply to a work as a whole instead of snippets, e.g. if your
project has a few generated functions it could still have a copyright.  If instead
you instruct an LLM to "make a game" (and it's able to do so), that could would
not be copyrighted.  As an example, ["Zaraya of the Dawn"](https://www.copyright.gov/docs/zarya-of-the-dawn.pdf)
is a comic book where the images were produced by Midjourney.  While the text
and layout were human-generated and therefore subject to copyright, the US
Copyright Office found the images could not be copyrighted.  Extending this to
software, if you have AI produce all of your UI, that portion of your code might not be copyrightable.

If you are developing code you intend to monetize, the safest advice currently would be
to avoid LLM-generated code altogether.  Were it brought to light in discovery,
AI-generated code could open the door to damages over the entire code base.
Otherwise, treat LLM output like code from an internet forum, you can use it
for information and to point you towards the code you need, but don't copy its
entire output.  If you do copy and paste code, you may also want to mark in the
source code what is LLM-derived.  Doing this consistently could safeguard parts
of your project that may resemble proprietary code by chance.
