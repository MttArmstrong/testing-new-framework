---
title: "Documenting Your Choice of License"
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


* Once you’ve chosen a license, you should ensure that it is indicated clearly in your software and documentation.
    * A LICENSE file in the repository is a common starting point.  Typically it contains the actual text of the chosen license.
    * Best practice is to also mark individual source code files with copyright notices at the top of each file.  Whether you need to include the entire license is debatable.   You can probably refer to the text of the license elsewhere, along the lines of “License: 3-clause BSD, see file LICENSE”.

## Managing Copyright Notices in Software

* All this does no good if you don’t make the license you’ve chosen clear to all
* Need to  **assert copyright** and make  **license terms**  explicit
* Do these centrally or in every file?
  * Single COPYING or LICENSE file per package (or directory)
  * In comments at the top of the file
  * Advantages and disadvantages to each
* ***Best practice: do both***
  * Intelligently, to make it as easy to maintain as possible – script updates!
* Authorship (separate, but related)
  * Version control is best way to maintain accurate records of authorship
* See [Managing Copyright Information within a Free Software Project](http://softwarefreedom.org/resources/2012/ManagingCopyrightInformation.html) for details
* Also [Software Package Data Exchange](https://spdx.org/) (SPDX, emerging standard)

{% include links.md %}
