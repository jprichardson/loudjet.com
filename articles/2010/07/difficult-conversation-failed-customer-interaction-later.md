<!--
id: 821807701
link: http://loudjet.com/a/difficult-conversation-failed-customer-interaction-later
slug: difficult-conversation-failed-customer-interaction-later
date: Fri Jul 16 2010 21:27:00 GMT-0500 (CDT)
publish: 2010-07-016
tags: consulting, truck-software, business-lessons, golden-rule, customer-service
-->


Better to Have a Difficult Conversation Now, Instead of a Failed Customer Interaction Later
===========================================================================================

![](http://media.tumblr.com/tumblr_l5ok4r1rnr1qzbc4f.png)

Whenever one of my college friends comes back into town, I love to call
everyone from the old crew to go out and get some drinks. One of these
friends, who we’ll call “Sergey” always responds enthusiastically by
saying “yea man… I would love to meet up with you guys. I just have to
do a few things and then I’ll give you a call!” Nine times out of ten,
Sergey never shows up. On the times when he doesn’t show up, he doesn’t
even send a text or call to let us know that he’s not coming.
Admittedly, I feel a bit let down. I’ve told Sergey that it would be
nice if he would just shoot me a text telling me that he can’t make it.
I understand he’s busy and has obligations but I think it’s common
courtesy to let someone know you can’t make it if you say you will.

Earlier today, I was reading my typical [RSS
articles](http://loudjet.com/a/less-consumption-more-production).
I read Seth Godin’s latest article[A Hierarchy of Failure Worth
Following](http://sethgodin.typepad.com/seths_blog/2010/07/a-hierarchy-of-failure.html).
It’s small enough, I’m going to include the whole text:

> Not all failures are the same. Here are five kinds, from frequency =
> good all the way to please-don’t!
>
> FAIL OFTEN: Ideas that challenge the status quo. Proposals.
> Brainstorms. Concepts that open doors.
>
> FAIL FREQUENTLY: Prototypes. Spreadsheets. Sample ads and copy.
>
> FAIL OCCASIONALLY: Working mockups. Playtesting sessions. Board
> meetings.
>
> FAIL RARELY: Interactions with small groups of actual users and
> customers.
>
> FAIL NEVER: Keeping promises to your constituents.
>
> The thing is, in their rush to play it safe and then their urgency to
> salvage everything in the face of an emergency, most organizations do
> precisely the opposite. They throw their customers or their people
> under the bus (“we had no choice”) but rarely take the pro-active
> steps necessary to fail quietly, and often, in private, in advance,
> when there’s still time to make things better.
>
> Better to have a difficult conversation now than a failed customer
> interaction later.

After the the “Fail Never” line, I started thinking about one of my
clients. After the last line, I got some knots in my stomach. You see,
I’ve been a software consultant/contractor for about four years. I’ve
been working with a trucking company to develop software to
manage/schedule their fleet since I started consulting. I “finished” the
software about two years ago. They’ve called me from time to time to do
some small updates. About three months ago I got a call from them asking
me to do some other updates. I visited their office and discovered that
they didn’t really use the software much, and when they tried, it didn’t
work as expected. It would crash, the UI would lock up, and it was
generally buggy. I made a ton of mistakes:

1.  I made a custom
    [ORM](http://en.wikipedia.org/wiki/Object-relational_mapping) around
    PostgreSQL. At the time, I didn’t even know what an ORM was, I just
    thought it made sense to wrap up the database layer into nice pretty
    classes.
2.  I wasn’t too familiar with [design
    patterns](http://en.wikipedia.org/wiki/Design_pattern_%28computer_science%29)
    or [unit testing](http://en.wikipedia.org/wiki/Unit_testing).
3.  My strategy was basic drag & drop using [Windows
    Forms](http://en.wikipedia.org/wiki/Windows_Forms) and C\#.
4.  I mixed business logic and UI programming. I even put blocking
    networking code in the UI thread!

My major strength was that I had a great grasp on simplicity and UI
design. The app itself looked great. But, you can polish a turd and it’s
still a turd. Regardless though, this wasn’t even my major weakness. As
a developer (or as an optimist?), I frequently give clients optimistic
time lines for completion of projects. This time was no exception. “Yea,
we’ll come out at the end of a next week and show you the updates.” I
said. When I opened up the code and looked at it again, I knew I was in
trouble. What the fuck was I thinking years ago when I wrote this?

I worked diligently. The end of the next week came. I still wasn’t done.
Not even close. Try making small changes to your data model on your
crappy custom ORM. It sucks. I really wanted to rewrite everything, the
whole entire app. But, I knew that would lessen my chance for success,
as most of the functionality works. [I knew that was a bad
idea](http://www.joelonsoftware.com/articles/fog0000000069.html).

The week passed. I didn’t call them. It’s not like I blew them off, as
we didn’t have a time scheduled, just a “end of next week” time. The
following week passed without me contacting them. After reading that
last line, I knew I had messed up.

> Better to have a difficult conversation now, instead of a failed
> customer interaction later. -Seth Godin

Don’t forget this. Seriously. I called them almost immediately after I
read that line. I knew I needed to tell them that I’m still working on
making it work well and that I didn’t forget about them. They were very
grateful that I had called and were willing to wait longer. When it
comes down to it, they could have picked anyone else, but they picked
me. I should not take that for granted.

Much like I was let down when my friend Sergey wouldn’t let me know that
he wasn’t going to make it, I let my client down. That’s bad business. I
won’t ever end my friendship with Sergey because I enjoy hanging out
with him as we’ve been friends for about 15 years, but the truck company
could’ve ended their relationship with me years ago.

But the real lesson is that business is about relationships. Each
business interaction should be treated as such. If you can manage your
business relationships in a uniquely positive manner, you’ll be
successful. So many companies out their treat their customers like shit.
Don’t be this company. Use the [Golden
Rule](http://en.wikipedia.org/wiki/The_Golden_Rule) on this one and your
customers will love you for it.

Follow me on Twitter: [@jprichardson](http://twitter.com/jprichardson)

-JP Richardson

