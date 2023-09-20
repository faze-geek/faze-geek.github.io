---
title: Starting GSoC 2023
layout: post
description: null
image: null
open_blog: true
suburl: "2023/05/13/a_Starting_gsoc.html"
---

I am very happy to share with you that on 4th May, 2023 I was accepted as a
GSoC student of [SymPy](https://www.sympy.org/). I would be working on control module under the guidance
of my mentors, [Smit Lunagariya](https://github.com/Smit-create) and [Nikhil Maan](https://github.com/Sc0rpi0n101).

I have interacted with Smit before on a different project named LPython. We had discussed a couple of issues. I look forward to interacting with Nikhil too. I have no doubt in my mind that working under their guidance will be a great learning experience for me.

As of now my end semester exams and results are going on. I expected the selection email being one of the happiest moments in my life but having to prepare for a tough exam the following day, I was busy keeping up with the portion at 12:30 am. I hardly celebrated for 15 minutes :)
I have set up my blog today by forking this [repository](https://github.com/czgdp1807/czgdp1807.github.io) from [Gagandeep Singh](https://github.com/czgdp1807). He is a previous contributor to SymPy and well known in the community.

---
**Coding Period Ends**
.... Hello everyone, hope this blog finds you well.

I am writing this blog 2 weeks since the previous blog as I had my minor exams at university last week. Having pushed all the code I proposed, I did not have any major changes to make and could focus on my exams. Implementation and testing of the State Space Model is complete from my end. I believe that I have addressed all the reviews and it is close to being merged into the codebase. Although the coding period has ended, it is still my responsibility to make sure that our work eventually goes in. 

**Aim :**

This week I made some comments towards the **State Space model**. It can be viewed [here](https://github.com/sympy/sympy/pull/25473). 

**Work : Let us go through the Pull Requests in brief.**
1. Failing Test: \
   If you go through the latest developments on this [comment](https://github.com/sympy/sympy/pull/25473#discussion_r1326286494), there are some tests which fails due to the modified behavior of floats. I am having some difficulties in figuring out why these asserts are failing with `sympy.evalf()`.

   ```
     p1 = a1*s + a0
     p2 = b2*s**2 + b1*s + b0
     G = StateSpace(Matrix([p1]), Matrix([p2]))
     expect = StateSpace(Matrix([[2*s + 1]]), Matrix([[5*s**2 + 4*s + 3]]), Matrix([[0]]), Matrix([[0]]))
     expect_ = StateSpace(Matrix([[2.0*s + 1.0]]), Matrix([[5.0*s**2 + 4.0*s + 3.0]]), Matrix([[0]]), Matrix([[0]]))
     assert G.subs({a0: 1, a1: 2, b0: 3, b1: 4, b2: 5}) == expect
     assert G.subs({a0: 1, a1: 2, b0: 3, b1: 4, b2: 5}).evalf() == expect_
   
     >>> G.subs({a0: 1, a1: 2, b0: 3, b1: 4, b2: 5}).evalf() == expect_
     False
     >>> print(G.subs({a0: 1, a1: 2, b0: 3, b1: 4, b2: 5}).evalf())
     StateSpace(Matrix([[2.0*s + 1.0]]), Matrix([[5.0*s**2 + 4.0*s + 3.0]]), Matrix([[0]]), Matrix([[0]]))
     >>> print(expect_)
     StateSpace(Matrix([[2.0*s + 1.0]]), Matrix([[5.0*s**2 + 4.0*s + 3.0]]), Matrix([[0]]), Matrix([[0]]))
  

**Future Work :**
Now I have reached my last official active week for Google Summer Of Code, I have to make my final work product submission. That will be followed by the final evaluations. It has been an amazing journey with a few final touches remaining.
