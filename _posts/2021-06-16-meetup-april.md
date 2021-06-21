---
layout: post
image: '/img/shane-aldendorff-mQHEgroKw2k-unsplash.jpg'
title: "A demo in the life of an RSE"
excerpt_separator: <!--break-->
date: 2021-06-16
---
*Photo by <a href="https://unsplash.com/@pluyar?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Shane Aldendorff</a> on <a href="https://unsplash.com/s/photos/mechanism?utm_source=unsplash&utm_medium=referral&utm_content=creditCopyText">Unsplash</a>*

Authors:  
[Lieke de Boer](https://twitter.com/liekedb) / Netherlands eScience Center  

If you’re curious about the kinds of things a Research Software Engineer (RSE) can get done when employed in that capacity, you’d have enjoyed the April 2021 NL-RSE meetup, where we saw the demos of two RSE software projects. [Paul Konstantin Gerke](https://rse.diagnijmegen.nl/members/paul-konstantin-gerke/), RSE from the diagnostic imaging analysis group (DIAG) at Radboud UMC, gave a demo of the [Grand Challenge](grand-challenge.org). The Grand Challenge is a Python-based platform where researchers and engineers can annotate and analyze medical images to, for example, judge the likelihood that a patient has a COVID-19 infection, based on a CT scan of that patient’s lungs. The platform also allows users to compare their own medical imaging machine learning algorithms to those of others. The Grand Challenge website lists different leaderboards for several “challenges”, or medical imaging machine learning problems, and ranks the performance of competing algorithms for each challenge. 

[Casper Kaandorp](http://uva-aias.net/en/staff/casper-kaandorp), RSE from Utrecht University, presented the second demo: NIDM (Networking during Infectious Disease Model). NIDM is an Elixir web application that can be used for running social experiments. Casper demonstrated a social risk-taking behavioral experiment, which consisted of the simulation of an infectious disease spreading through a social network. Study participants are supposed to earn money by befriending others in their network, while minimizing connections with infected individuals. Believe it or not, the app was conceptualized before the COVID-19 pandemic.  

The demos were followed by a panel, where the meeting chair Carlos Martinez-Ortiz asked the two RSEs how their respective RSE groups are set up, and what challenges they have faced. Below is a summary of their conversation.  <!--break-->

### How is your RSE group set up? 

**Paul:** My group is part of the DIAG: the research arm of the Radboud UMC radiology department. The DIAG consists of about 60 people, split up into teams of 5-10 people with different research specialities. The RSE group is one such team. Our RSEs take on work that can address common goals between multiple DIAG research teams. The research team leaders establish common goals in a panel, and the RSE group tries to implement software features in line with the goals communicated by the panel. This is how the RSE group has built the Grand Challenge, a platform that can be useful for all research teams.  

**Casper:** I am part of a group of RSEs that is helping researchers from all backgrounds at the Utrecht University with different kinds of problems, so our approach is broader than what Paul describes. The range of projects we work on is immense, from easy projects like setting up a GitHub repository, to helping people with machine learning projects that are extremely complex.  

### What kind of resources does your RSE group have, and is that enough? 

**Casper:** At the moment, funding is not a problem for our team of 10 people. There’s a cap on how many people can work in our group, though. Our team grew in the past months, so our capacity is currently increasing, but we can’t take on new projects too fast, because we never know what kind of project may come to us. Any kind of task can come up, which makes the job interesting, but also unpredictable, and can leave us overwhelmed with work. 

**Paul:** Our RSE group is facilitating research funded by NWO. To add features to the platform, we should be fulfilling researcher needs, and working in line with the available funding. There is also another funding stream however: there are industry partners (AWS for example, for cloud expenses) that provide resources. But we also develop and market medical products, which brings in money.  

### Is there a limit on time and budget that you spend on different projects? 

**Paul:** We want attach deadlines to feature development, because ever-ongoing projects can be a problem. When you’re given one year to finish a project, that project will be on the backburner, and can forever be pushed back. The time and money we spend on features is determined by what our stakeholders want, and what the panel decides we should work on. For example, a stakeholder may want our software to include Magnetic Resonance (MR) support. We then decide that in order to provide that, we need to implement feature A, B and C. We bring our proposal for feature A, B and C back to the panel, who may tell us to focus on feature A. Then we like to commit a set amount of time to developing feature A.  

**Casper:** At UU, our coordinator tries to put a minimum of 2 people on each project, so no one works alone. Sometimes it is unavoidable for someone to work alone on a project, though. This can be an issue, but when you are with so few people and such a variety of projects, it’s sometimes impossible to structure it differently. We used to have an undefined amount of time for any given project, which often meant that projects would take more than half a year to get done. We now have a rule that a project should be finished within half a year of one person’s full time amount of work. A common challenge we still face is that we may start working on a project, but the researcher who approached us becomes busy with something else, and the project is left for some time. The researcher sometimes comes back and expects the RSEs to pick up where they left off, which is then often impossible.  

### What kind of projects do researchers approach you with?  

**Casper:** We get requests from every kind of researcher there is. Half of those requests lead to nothing, because the researcher isn’t ready yet. A quarter is consultancy and includes helping researchers with questions about how to set up a job on Lisa (HPC system at Utrecht University). These are the type of questions that can be solved in a few days.  

The last 25% is wild. It can be anything. Recently, there was a researcher who went to the Congo and recorded two types of audio. One of jungle sounds, in the wild, and another of sounds from a monkey sanctuary. They then came to us with the question if it would be possible to create an algorithm that could predict biodiversity in each surrounding based on these recordings. So we helped them to do this.  

I also worked on a project that looked at betting behaviour in sports bets, which is similar in some ways to betting in the context of the stock market. The application we developed browsed bookmaking websites to get a feeling for betting odds in sports matches. The application would bet very heavily on one contestant when the odds were 50/50. The goal of this was to try and see if the application could “swing the market”, so other participants would follow the application’s lead. Eventually, there was a very small significant effect of our betting, meaning that people did follow the application’s bets. I was hoping we’d make some money with it, because during the first two months we won quite a lot! Unfortunately, we lost a lot later on. It was a really interesting project, but not a profitable one.  

**Paul:** The work we do at the DIAG may look very focused, but that was the RSE trick: We stripped all the focus away, and ended up with a generic solution for different fields. We don’t tackle the very specific things anymore. What Casper says is right; with a lot of different projects, it’s easy to get completely overwhelmed and not finish things. This is where our structure really helped us out.  

### What’s staffing and managing an RSE group like? How do you find the right person to hire, and how do you convince funders to keep funding you? 

**Paul:** It’s definitely untreaded territory. Recently our group grew a lot, to 11 RSEs in total. We’re still learning how to manage such a team. It can be quite difficult to find the right employees. We’re in the East of the Netherlands, and as a hospital, you compete with industry for software engineers who have the skills that you need. It’s common that those candidates move to the Randstad if they get a good offer there.  On top of that, operating from a hospital has its own challenges. Hospitals are not really known for building software - they’re geared to patient care, and maybe research, but not software development.  

Our future strategy will be to work more as a remote team. We now have had one year of practicing working remotely of course, because of the circumstances in the COVID-19 pandemic. And there are many benefits to RSEs who work with us. The work is meaningful, challenging and interesting, and the hospital is a flexible workplace.  

### Closing remarks 

Thanks to Casper and Paul for participating in this panel and for sharing their diverse experiences being part of RSE groups. 

Are you an RSE working in a group? Is the structure of your group different from what is described here? We would love to hear your experiences! 
