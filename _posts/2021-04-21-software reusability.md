---
layout: post
image: '/img/maria-shanina-dWHeuGw0fBM-unsplash.jpg'
title: "What is really needed for software reusability?"
excerpt_separator: <!--break-->
date: 2021-04-02
---
*Photo by <a href="https://unsplash.com/@mariashanina?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Maria Shanina</a> on <a href="https://unsplash.com/?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>*

Authors:  
[Faruk Diblen](f.diblen@esciencecenter.nl) / Netherlands eScience Center  
[Barbara Vreede](b.vreede@esciencecenter.nl) / Netherlands eScience Center  
[Daniela Gawehns](gawehnsd@liacs.leidenuniv.nl) / Leiden University  
[Carlos Martinez](c.martinez@esciencecenter.nl) / Netherlands eScience Center  

Writing software has become one of the most important parts of the research process. In its simplest form, research software is a single script that can, for example, be used for collecting, processing and/or visualising data. Complex analyses and workflows are consolidated into larger pieces of software that are often the result of research and the subject of papers. The increasing importance of computer code in research is highlighted by the growing level of attention to software from the European Open Science Cloud[^SIRS] and the OECD Recommendation on Access to Research Data which now includes software[^OECD].
<!--break-->

[^SIRS]: E. C. D. G. for Research and Innovation., Scholarly infrastructures for research software: report from the EOSC Executive Board Working Group (WG) Architecture Task Force (TF) SIRS. LU: Publications Office, 2020. [https://data.europa.eu/doi/10.2777/28598](https://data.europa.eu/doi/10.2777/28598) 

[^OECD]: Alan Paic, Making data for science as open as possible to address global challenges [https://oecd-innovation-blog.com/2021/01/20/oecd-recommendation-access-research-data-public-funding-update-covid-19/](https://oecd-innovation-blog.com/2021/01/20/oecd-recommendation-access-research-data-public-funding-update-covid-19/)

One of the missions of the Netherlands eScience Center is promoting software reuse. In order to improve research software reusability, the Center’s Software Sustainability SIG (Special Interest Group) compiled a reusability checklist for research software (see Table 1). The checklist is meant as a minimum list of requirements that one would expect to see (as a user) in order to be able to use a given piece of software (whether it is a library, or a single script). The checklist covers aspects such as documentation and licensing.

**Note**: reusability can be easily confused with another important term: reproducibility. The two are closely related, but not quite the same: the former is an important component of the latter, but software need not be reusable to be reproducible. Roughly speaking and for the purpose of this blog: we talk about reproducibility when the same code and same data are used to produce the same results; we talk about reusability when the same code is used with different data to produce new results (read [detailed discussion](https://github.com/NLeSC/guide/discussions/237)). The software reusability checklist is aimed primarily at reuse, but it may also be applicable to ensure reproducibility of scientific results produced by the use of software.

***

The following is the set of minimum requirements we defined for code to be **repeatable**, **re-runnable** and **portable**[^reproducibility]:

**The software**:
 - is in an accessible repository, preferably version controlled;
 - has a license (see: ‘The license’);
 - is documented (see: ‘The documentation’).

**The license**:
 - allows for reuse;
 - is compatible with the dependencies’ licenses.

**The documentation**:
 - has installation instructions, including good descriptions of:
   - the hardware it depends on (e.g. GPUs);
   - the operating system the software has been tested on;
   - software requirements (libraries, shell settings, etc).
 - explains usage, specifying:
   - what the software does;
   - how it can be used;
   - what options/parameters are available.
 - contains examples of how to run it.

**Finally**:
 - If the software depends on any sort of data, the data should be available

[^reproducibility]: J. Freire and F. Chirigati (2018) Provenance and the Different Flavors of Computational Reproducibility. Bulletin of the IEEE Computer Society Technical Committee on Data Engineering, Vol 41, no. 1, p.15-26 [http://sites.computer.org/debull/A18mar/A18MAR-CD.pdf#page=17](http://sites.computer.org/debull/A18mar/A18MAR-CD.pdf#page=17)

***
Table 1. Minimum requirements list for software reusability

***


### eScience Center Reusabilithon

We had initially planned to hold the Reusabilithon with a relatively large group of eScience engineers, as part of our internal activities. However, with the lockdown affecting our capacity early 2021, we changed our plan. Instead of canceling the event, we decided to carry out the event online, and on a small scale. As a bonus, this helped against the lockdown-induced boredom, by breaking the routine and spending some time doing something interesting and fun! 

Two eScience Center RSEs worked together via Teams for one afternoon. They applied this list to 3 different pieces of software ([sv-callers](https://www.research-software.nl/software/sv-callers), [muscle3](https://github.com/multiscale/muscle3) & [iScore](https://github.com/DeepRank/iScore)) developed in-house. The following are the observations by the engineers in this small reusabilaton:

> “It took us about 1 hour per use case working together, and most time was spent getting the example to work. Independently from how each tool did, we found that the minimum requirements list is fit for purpose – no points in the list felt to us as if they should be left out; we also did not feel that there was something missing in this list.
> 
> One point which we did find challenging: it is not easy to determine at a glance if there are any conflicts with the dependencies of the software. It could be helpful to have a check or remark that dependencies have compatible licenses”

This experience describes an encouraging first experiment. However, it was conducted on a very small scale, and by engineers who were vaguely familiar with the software in question.

As a follow up, a discussion session during the [NL-RSE meetup](https://nl-rse.org/events/2021-02-11-meetup.html#software-re-usability--what-is-needed) led to the writing of this blog post. The Software Sustainability SIG would like to organise a larger *reusabilithon* with participants from a broader audience and from a wider range of organisations; very similar in format and spirit to the already successful [Reprohack](https://reprohack.github.io/reprohack-hq/). However, where the latter focuses on the *reproducibility* of research results, during a reusabilithon participants and aim for reusability. As explained earlier in this post, we understand *reusability* to be using existing code on new data (even if such data is just parameters).

One of the aims of a future *reusabilithon* is to gather more feedback on the suitability of the current reusability checklist and improve it. The long-term aim of such a list is to provide researchers with a useful tool to be able to improve the reusability of the software they produce.

The long term aim of running a *reusabilithon* is making RSE's (and researchers writing research code) aware of what reusability is about and to develop their expertise in using tools to improve reusability. In the future, some of the checks in the reusability checklist could be automated by using tools such as [howfairis](https://github.com/fair-software/howfairis), [fairtally](https://github.com/fair-software/fairtally), [fossa open source compliance management](https://fossa.com/product/open-source-license-compliance), [GFZ software quality assurance](https://gitext.gfz-potsdam.de/software/services/fair/software-quality-assurance), etc. We expect the reusabilithon can help identify additional tools that can automate some checks. However instead of automating everything from the start, we need to validate that the points in this checklist are indeed useful for software reuse.

### Are you interested in participating in future reusabilithons? Contact us!
Dear reader, if you are involved in developing research software -- whether it is in the form of small data analysis scripts or complex libraries -- and you would like to participate in future reusabilithons, please leave a comment or [send an email](mailto:c.martinez@esciencecenter.nl), and join our effort!
