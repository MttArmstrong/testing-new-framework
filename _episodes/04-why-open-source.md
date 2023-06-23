---
title: "Open Source Licenses for Scientific Software"
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

* Open source licensing is widely (though not exclusively) used in the scientific software community.
    * Visibility into the software producing scientific results is considered by most to be consistent with the scientific method.
    * Many may see open source licensing as an approach to sustainability of the software – getting others to contribute.  This is magical thinking, and rarely happens in practice. Open source licensing is (probably) necessary, but not sufficient to attract outside contributors.


## Considerations Favoring Open Source

* Challenges of managing and archiving the paperwork associated with proprietary licenses

* Explicit license agreements can inhibit (legal) use of software

* I want to support peer review and reproducibility in science

* My sponsor requires that I release my software as open source

* I believe that the results of publicly-funded research should be publicly available

* I want to build a self-sustaining community around my software


## Consideration: Software Business Models

| Approach | Proprietary | Copyleft  | Permissive  |
| :-: | :-: | :-: | :-: |
| Sell the software | yes | yes | yes |
| “Fremium” or “dual licensing” allows free use by some, paid by others | yes | yes | yes |
| Relicense to proprietary | n/a | no | yes |
| Sell convenience, e.g., packaging, installation media, pre-compiled executables | yes | yes | yes |
| Sell professional services around the software, e.g., training, technical support, consulting | yes | yes | yes |
| Sell custom development services, e.g., proprietary extensions, accelerated development | yes | yes | yes |
| Sell software-as-a-service (SaaS) | yes | yes | yes |
| Sell the research | yes | yes | yes |

## Consideration: Don’t Want Others to Profit from my Open Source Software

* A permissive license allows someone else to take derivatives proprietary
* A copyleft license will prevent that

**But there may be other considerations…**

* What if you  *do*  want a commercial entity to use your software?
  * Exposure, broader distribution
* Copyleft is scary to many commercial entities
  * How far does the viral license reach into other parts of the product?
  * Legal opinions differ, no case law yet
    * Lawyers will tend toward a conservative answer: avoid copyleft software
    * *Experience: some companies will not consider working with copyleft software*
    * *Experience: some companies consider staff working on copyleft software to be “contaminated” and will not allow them work on other software*
* Even in non-commercial environments, copyleft may raise compatibility concerns

## The Software-as-a-Service Conundrum

* Many software-as-a-service (SaaS) products make extensive use of open source software
* Some software developers don’t like the possibility that another company can trivially monetize (other people’s) software by turning it into a SaaS product
  * It may compete with their own SaaS offerings
  * The SaaS provider can keep enhancements proprietary and while making the benefits available in the SaaS product
* Attempts to curb this via licensing result in licenses that are not open source
  * In some cases, key modules are changed to proprietary licenses, while others remain open
* See: [https://arstechnica.com/information-technology/2019/10/is-the-software-world-taking-too-much-from-the-open-source-community/](https://arstechnica.com/information-technology/2019/10/is-the-software-world-taking-too-much-from-the-open-source-community/)

## Consideration: Protecting my Intellectual Property

* If I make my source code freely available, then others can use the novel ideas embodied in it to “scoop” me
* Proprietary licenses (obviously) allow you to keep source private
* Open source licenses don’t require that you make derived works public, only that  *if*  you do, you make the source available
* Delay public release until you’ve had a reasonable chance to exploit the results of your work
  * Until initial papers are published
  * Fixed time period (e.g., one year)
    * A similar compromise is sometimes used in academic publishing: sponsor may want open access but allow publisher a proprietary exploitation period (often 1 year) before making it openly available
    
{% include links.md %}
