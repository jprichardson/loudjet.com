<!--
publish: 2013-03-31
tags: gitpilot, corey, brian, reflect7
author: JP Richardson
-->


Gitpilot Postmortem
===================

Deciding to close down a company is rarely an easy decision. The purpose of this post to analyze the failure of Gitpilot. Unfortunately, it will not serve as an entertaining narrative as I need to get these raw thoughts out before they fade away; it's already been three months since we've terminated the company. However, it does serve as a great reference on lessons-learned for my ex-cofounder Corey and me.

Let's revisit how Gitpilot came about. If you want to see any of the demos of Gitpilot, scroll-down to the bottom and look under `Media`.



Genesis
-------

Corey, Brian, and I founded Reflect7 in 2009 to bring sports' information such as schedules, roster, etc to fans on the iPhone. Corey and I were the primary developers on the projects; we were big fans of [agile methodologies](http://en.wikipedia.org/wiki/Agile_software_development). In particular, we used a simplified system of writing our action items for the upcoming week and documenting our accomplishments from the previous week. Ideally, all action items were accomplished.

We typically used either Google docs or email to keep track of action items and accomplishments. It felt unwieldy. How productive were we really? Wouldn't it be great to see if Corey completed a task or had started working on a task? What if there was a way to tie each task to our code repositories? Would that help us to see inefficiencies and improve upon them? It makes me feel good about completing things by leveraging my [compulsive nature](http://loudjet.com/a/use-a-weakness-to-develop-a-strength/) to make a list and check shit off.

Eventually we sold Reflect7, we were pondering on what to do next. I was on the hunt for the perfect productivity solution.

I told Brian and Corey the story of how [Buffer validated their idea](http://loudjet.com/a/a-real-mvp-tale/) without having have built more than a landing page. Corey then thought it'd be cool to build a concept of Git integrated with project management. Corey came up with the concept and named it Gitpilot. He created a simple landing page with mocked up screenshots, listed the benefits of Gitpilot, and put a textbox to register an email address. We submitted it to a few social media sites and within a few days, had 250 visitors!



Gitpilot the Web App
--------------------

Brian moved on to work on his own startup that he had built up before we sold Reflect7; Corey and I felt that the 250 users validated the idea. So we formally incorporated Gitpilot LLC.

Gitpilot started out as a web app. The idea is that you'd download a cross-platform daemon (background-program) that'd hook into your Git repo and notify the site of changes. We thought that the web app would be ideal as devs were use to interacting with Git repos because of Github and we'd be able to target all platforms from the start.



Development with Colleagues Becomes Easy
----------------------------------------

Gitpilot was intended to solve a few problems:

1. Developing software with your colleagues using Git can be difficult. How do you coordinate development? Do you develop on the `master` branch? [git-flow](http://nvie.com/posts/a-successful-git-branching-model/) became a common model of developing software. But it still didn't quite make it clear on how to best develop software with others.

2. Git itself can be difficult for beginners. This was the most common complaint that we heard about dev starting to use Git. If we could solving #1 would solve #2 as well.

In short, version control, such as Git tells you **who** did what, but it doesn't instruct you on **how**. We wanted to make it effortless. A dev should not have to care if their on the `master` branch or the `developer` branch. A dev should just focus on the current feature or bug fix.

So we developed a vision for Gitpilot. We envisioned a world where you'd start coding and working with a team would come near effortless.

We envisioned software that was like a real-time collaborative Git GUI for git-flow. Hopefully that doesn't too much like the [Start-up Guys](http://www.youtube.com/watch?v=LMmdl4VltD4) But, it was never intended to be a Github competitor, but a Github compliment.



Evolution to a Mac App
----------------------

We realized that a web app might not be the best place to start. Two developers might not be able to support cross-platform very effectively from the beginning. We needed to simplify.

Perhaps Apple's marketing caught us, maybe our Objective-C roots started to permeate themselves from our history at Reflect7, but we thought it'd be a good idea to pivot Gitpilot into a Mac App. The Mac app would allow us to do the following:

1. Focus on a small subset of developers. We were OK with this for launching.
2. Get revenue immediately.
3. Integrate with Git much easier than a web app could.

This decision came about after about four-months of development around November of 2011.

Maybe I should have heeded my own advice a bit more: [It's All Our Fault: Why Building a Business on the Apple App Store is a Losing Proposition](http://loudjet.com/a/its-all-our-fault-why-building-a-business-on-the/)

Apple announced their sandbox restriction for new Mac Apps. So we had to spend additional time to navigate around that. That was a huge pain in the ass.

By around May of 2012 or so we were able to launch a beta into the Mac App store. Over the months, we collected more email addresses to out Gitpilot landing page. We had over 600 at this time. We put a price of $80 intentionally thinking that it'd be set too high for anyone to buy it. We sent out an email to our list with some questions asking about their current development operating system and what their biggest problems with Git were. We then sent out 50 promo codes. 

To our surprise, $80 did not prevent people from buying it. However, not one of the people who bought it contacted us on any problems or issues. But we did get feedback from some of the people who we sent out the promo codes to. As an aside, we thought that anyone that received a promo code for software that had a $80 price tag that they would be more inclined to test it, since they may associate $80 worth of software for free. It should be noted, that this wasn't the case. Of the people we got feedback from, one recurring theme stood out: there was too much Git magic going on with the repositories. 



Iteration
---------

We had an initial law of Gitpilot that stated: developers must have absolute faith that Gitpilot will not screw up or mess up developers' code without them knowing what's going on. From the feedback, it was clear that we had violated that.

We modified Gitpilot in three ways:

1. We made it dramatically simpler by chopping out features.
2. We notified the user of every Git action by an unobtrusive "dick bar" (a small non-modal overlay at the top of the window that prompted the user to action).
3. We added a contact form built into the app that enabled the user to open up their email client and send immediate feedback. We did this same thing in our iPhone apps for Reflect7 and what felt like an email every 5 to 10 mins. 

We sent out another email to our list and submitted some more articles to social news sites. Very little response.

People were importing their repos and adding some improvements to their `develop` list, but very little action was taken. No one invited users to join them. We built a seemless user invite system into Gitpilot.



Price Drop to $50
-----------------

Increase in sales, zero feedback.



Price Drop to $20.
------------------

Further increase in sales, but still zero feedback. Weren't any of these customers pissed off that things didn't work or happy that they found the solution to their dreams?



Using Gitpilot with Gitpilot
----------------------------

Corey and I were dumbfounded. We found the software useful. It promoted friendly competition between the two of us. If Corey had gotten most his action items done for the week, then I'd push myself to get my action items done. We thought about adding some gamification to the app, but it felt too premature.

When talking to more people, it seemed that there was massive confusion. Was it a Git GUI? Was it a project management with Git integration? Does it even solve my pain points? Was real-time even necessary or a benefit?



Price Drop to Free
------------------

We thought we'd do this and keep the beta label, but see if we'd generate a storm of feedback. We just wanted feedback. Over the course of a few days, we had thousands of downloads! We had maybe three emails.

It was clear that since we weren't getting hate mail or love mail, people just didn't give a shit. That's the worse for a startup.



The Omega
---------

We decided that since people didn't care, that we should cut our losses and terminate the company before the end of 2012 for tax purposes. Gitpilot LLC was dissolved on Dec 31st, 2012.



Mistakes
--------

- When analyzing what Buffer did to validate their MVP, there is one subtle distinction that makes a world of difference. They actually had a "but it now" button on their site. When prospects would click it, a pop-up occurred that said "oops, you caught us before we're ready, but put in your info and we'll give you a discount when we're ready". Prospects had already committed to buying by clicking "buy it now." With spam filters as good as they are today, putting your email address into our landing page form didn't represent any sort of commitment. This might be the biggest lesson yet as it may have prevented us from starting the company originally.

- We should have talked to more prospective customers before writing a line of code. Did devs have the same problems that we did? If they did, we should have found at least 10 that would have agreed to purchase the solution when it was ready.

- I'm not so sure we should have pivoted into the Mac App store. At the time, it felt like a flash of brilliance of narrowing our potential customer base and generating revenue almost immediately. The web app may have solidified to out prospects that this isn't just some Git GUI. It's entirely different. They may have embraced it in a different way.

- We should have focused more on our sales copy on our home page. Maybe even A/B test. Ironically when we put up help videos on using various parts of the software, this had did not clear up confusion.

(I'm sure there's more, I'll add them as I think of them)




The Future
----------

The collaborative model that we developed while working on Gitpilot has value. We're not sure if we're going to open source the backend or even the GUI. I've started work on a Gitpilot command line app that integrates with Github as a backend that is intended to be open source, but I'm not working on a team at the moment, so my priority on this app has dropped dramatically.




Follow me on Twitter: [@jprichardson](http://twitter.com/jprichardson)

-JP 



**Media:**

- YouTube Videos: https://www.youtube.com/user/gitpilot
- [Gitpilot out to simplify organization, collaboration for developers](http://www.siliconprairienews.com/2012/11/gitpilot-out-to-simplify-organization-collaboration-for-developers)











