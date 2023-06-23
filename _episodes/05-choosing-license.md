---
title: "Choosing an Open Source License"
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

* The primary decision point in open source licensing is “permissive” versus “restrictive” (also referred to as “copyleft” or “viral”).  As with all software licensing, there are many considerations that may apply.
    * Permissive licenses allow derivative works to be released under a different license, even a proprietary one (though in practice, this is rare). Copyleft licenses require that derivative works be released under the same license as the original, although they do not require the release of the derivative works. (They can be kept private.)
    * Because of the “viral” nature of copyleft licenses, many commercial organizations prohibit use or dependence on copyleft-licensed software or libraries. For example, if you want an HPC vendor to be able to take your numerical library and optimize it for their platform and offer it as a “built-in” part of their software stack, you should probably choose a permissive license.

## Choosing a License

## Considerations in Choosing a License

* What rights do you want to retain or grant?
  * Who can use the program? (proprietary vs open)
  * Can users see the source code? (proprietary vs open)
  * Can users modify the source code? (proprietary vs open)
  * Can the users redistribute original or modified code? (proprietary vs open)
  * Can modified code be relicensed? (permissive vs copyleft)
* Compatibility with software under other licenses
  * Permissive licenses have fewer issues
  * [http://www.fsf.org/licensing/](error:ppt-link-parsing-issue)
* Labeling of derived works
  * Derived works must be identifieddifferently than original work
* Patent grant/retaliation
* Expectations of the community you want to engage?

* *Use an existing free/open source license rather than inventing a new one!*
  * *FSF and OSI certify many existing licenses (~80) as meeting their criteria*

## Popular OSI-Approved Licenses

| License | Type | GPL-Compatible | Patent Grant |
| :-: | :-: | :-: | :-: |
| Apache License 2.0  | Permissive | v3,not v2 | yes |
| BSD 2-Clause and 3-Clause licenses | Permissive | yes | silent |
| GNU General Public License (GPL) v3 | Copyleft | yes | yes |
| GNU Library or "Lesser" General Public License (LGPL) v3 | Weak Copyleft | yes | yes |
| MIT license (MIT) | Permissive | yes | silent |
| Mozilla Public License 2.0 | Permissive | yes | yes |
| Common Development and Distribution License | Permissive | no | yes |
| Eclipse Public License 2.0 | Weak Copyleft | yes | yes |
| Affero General Public License v3 (network use == distribution) | Copyleft | yes | yes |

## ChooseALicense.com (by GitHub)

* Primarily a decision-tree approach to helping you choose a license
* But backed by a repository with analysis of 30+ widely used licenses
* **The easiest way to access the whole list is to go to the “Appendix”**
  * **[https://choosealicense.com/appendix/](https://choosealicense.com/appendix/)**
  * A portion of the Appendix is shown at left
* This is implemented in a GitHub repository with Jekyll, and open to pull requests!

![]({{ page.root }}/fig/licensing1.png)

{% include links.md %}
