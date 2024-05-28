---
title: Community Bonding Period
layout: post
description: null
image: null
just_me: true
suburl: "2024/05/11/community_bonding.html"
---
Hello everyone, hope this blog finds you well.

As **Google Summer Of Code'24** has begun with a blast, here we are at the end of the Community Bonding Period.
This period is a process where newly selected contributors are welcomed within the community and given an idea about how Google runs GSoC. \
In the start of this period, there was an introductory meet with Google admins who explained us about the program and the various key factors that lead to a successful project. It was followed by a contributors summit where mentors and past GSoC'ers gave speeches. Although I started this phase a little late because of my ongoing endsemester exams, I have thoroughly enjoyed this phase .

Here is some of the work I did during this period - 
1. **Prerequisites**
- In this phase I switched up my development setup to a Mac OS machine from a Windows OS. I must say that the switch was not as seamless as I expected ! But after spending a couple of weeks with my Mac, I do feel comfortable with it :)
- I setup the [pocketpy](https://github.com/pocketpy/pocketpy) and [gsoc-2024-dev](https://github.com/pocketpy/gsoc-2024-dev) repositories locally. I can build the project successfully as of now. 
- Set up this blog to document my journey. I also made an account on Mastodom to post my blogs there, a neccessary component requested by organization admin [John Hawley](https://social.afront.org/@warthog9).

2. **Interaction with Mentors**
- I have been interacting with my mentor [blueloveTH](https://github.com/blueloveTH) on the pocketpy [discord](https://discord.com/invite/WWaq72GzXv) channel. You can join it as well, if you are interested in checking out the discussions and implementation plans for this project.
- Although we have not had a face to face meet on video, I hope we can have a chat soon. For now, we continue to discuss the tasks on discord itself.
- Another very important thing was communicated to us was that it is required of each student to submit a monthly report at the end of each month to [blueloveTH](https://github.com/blueloveTH). The monthly report should include our recent work and progress. I believe this will help the sub-org **pocketpy** to showcase it's work to various users and potential clients.

3. **Starting the Project**
- I started out by posting my GSoC'24 proposal on github. It is important that my ideas and timeline are clearly communicated to everyone and that's the beauty of open source. You can have a look at it [here](https://github.com/faze-geek/GSoC-24-Proposals).
- I have started brainstorming ideas with my mentors, the first modification we made to proposal was the go ahead with [xtensor](https://xtensor.readthedocs.io/en/latest/getting_started.html) over [NumCpp](https://dpilger26.github.io/NumCpp/doxygen/html/index.html). The major reason behind this is that NumCpp only supports 2D Arrays, which would greatly reduce the use cases of my project.
- Following that I have started to integrate **xtensor** in the **gsoc-2024-dev** project. We went ahead with the approach of directly copy pasting the headers from xtensor and it's dependencies. It doesn't take up much memory space in total, helping us to maintain the lightweight nature of our project.
- The pull request adding xtensor libraries can be viewed here: [Included headers from xtensor and xtl](https://github.com/pocketpy/gsoc-2024-dev/pull/2).

All and all it was a very useful phase of me. It helped me to settle in the pocketpy community as a contributor, make new connections and increase my network in the open source space. 

