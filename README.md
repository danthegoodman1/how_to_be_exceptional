# How to be Exceptional (or: how to get equity raises)

- [How to be Exceptional (or: how to get equity raises)](#how-to-be-exceptional-or-how-to-get-equity-raises)
  - [Agency](#agency)
  - [Unblocking your team is your default #1 priority](#unblocking-your-team-is-your-default-1-priority)
  - [Never be a single point of failure](#never-be-a-single-point-of-failure)
  - [Always seek to get better, and are not offended](#always-seek-to-get-better-and-are-not-offended)
    - [Always open to changing your mind](#always-open-to-changing-your-mind)
  - [Think like your users](#think-like-your-users)
  - [Understanding why](#understanding-why)
  - [Responsibility \& ownership](#responsibility--ownership)
    - [Dependability](#dependability)
    - [Availability](#availability)
    - [Context discovery](#context-discovery)
    - [Miscommunication hedging](#miscommunication-hedging)
    - [Use AI Often But Responsibly](#use-ai-often-but-responsibly)
  - [Other Resources](#other-resources)

I've always believed in merit-based compensation.

Team members that show increasing value to the team in multiple dimensions are the ones eligible for being given higher responsibilities among the business, and thus, higher reward (especially in the form of equity: "ownership mentality for ownership of equity").

When people have an ownership mentality, their game changes entirely. They become more effective, they think more holistically, the operate with more care, efficiency, and effectiveness.

Notice how you can always tell who the owner is at a restaurant?

Exceptional people are also the ones who get the most value out of their work. They grow the most as a person, and they stay longer at companies because they feel like they are able to get their best work done there.

This is a collection on some thoughts on what I think exceptional people do, and why they deserve to be disproportionately well-compensated.

This is what I think the ownership mentality looks like.

It's based on a combination of personal experience, and an obsession of observing the top-shelf of humanity: Not the household CEO names, but the "hands of the CEO", the ones who they delegate to, the ones who get shit done. Sometimes these people go unnamed for ages. Sometimes they go from intern to CEO.

Exceptional people are the opposite of mediocre and complacent. They are happy, but never satisfied. They're never "done". It really is the exceptional few that positively impact society in a meaningful way.

Because equity is ownership, only people who consistently work with an owner's mindset deserve more of it.

Build like your legacy depends on it. Own your domain, own problems, and own the outcomes. Follow-through to set yourself up for the next thing.

I've intentionally made this a git repo so it can be seen how my thoughts evolve over time.

## Agency

> _High agency is the single biggest predictor of outsized impact._
>
> _It means you act like an owner: you do what the company would do if it could momentarily clone the CEO and point them at the problem._
>
> _Owners don't wait, they don't hand-wave, and they don't need a babysitter._

**You find a way, not an excuse**
Constraints are real, but they're rarely immovable. You never just say "I/we can't do that", you say "… but I think we can do this".

**You treat every problem as yours until it's clearly owned**
"Someone else's problem" is never your first reaction. If you see a problem that's not already owned, you own it until it has the right owner.

If you're still confused how it applies, take this thought exercise: You somehow get stranded in the middle of nowhere. You know your really rough location, but you only have a single 5-min call before your phone dies. *Who do you call?*

Chances are, you'd call the highest agency person in your life. Because you know that regardless of whether they're the most equipped person, they'll loop in the right people, monitor the progress of action, and won't rest until you're rescued.

*This is the kind of person you should strive to be for your team.*

You should be the one that someone says "Hey I need something done, I think you're the most fit person to get it done, please help me."

High agency people also:

- Loop in people when they need help, don't suffer in silence
- Raise concerns early and often, rather than letting them become bigger problems with less time to fix later
- Link and update information without being asked for easy traversal of knowledge (notion to github issue, github issues closed, etc.)
- Write really good docs for code explaining
    - what it does
    - where and why it's used
    - how it works

## Unblocking your team is your default #1 priority

> _An exceptional teammate's default #1 priority is to unblock the rest of their team._
>
> _If you're a bottleneck for your team, you are a problem. Your responsibility is to enhance your team, not impair them._

*But doesn't that prevent you from getting any work done?*

**No.**

The more time your team is spent blocked, the further reduced the output of the entire team is.

Let's take an example scenario:

- You are working on *thing*, it's going to take you N hours to finish
- Your team member is working on *other thing*, and they're stuck for what ever reason (bad docs, lack of knowledge, access to infra, etc.)
- They ask you for help because you are able to unblock them

There are two paths here that can be taken.

**Path 1:**

- You say "I'm working on something right now, I'll help you when I'm done"
- N hours go by (+N hours blocked)
- There's only 45 min left in the day, so you reconvene when you're both online tomorrow (+N+12 hours blocked)
- It takes 45min to fix (+N+12.75 hours blocked)

**Path 2:**

- You immediately pause what your are working on and help
- It takes 45min to unblock (+0.75 hours blocked)
- You go back to what you were working on, which finished 0.75 hours later than you intended

Obviously there is nuance to this, like if you're working on something that has a critical timeline and the other person is not, but you can see how by unblocking your team fast, the net time spent on things being unreleased is a difference of N+12 hours.

I could go into all kinds of manufacturing optimization theory and make an analogy that team members are like machines in a factory, but the above should be enough.

Specific to engineering, exceptional people perform review of other code first thing in the morning. They're bringing a fresh perspective, and it prevents them from

## Never be a single point of failure

> _Exceptional people ensure that they are not the only one who can do something,_
> _such that if they become unavailable, zero progress can be made._

Similar to [unblocking your team](#unblocking-your-team-is-your-default-1-priority), being a single point of failure (SPoF) in an organization should be avoided at all costs.

Removing SPoFs is a high priority task in distributed systems engineering, as well as organization building. An organization effectively is a distributed system, where you have components of teammates, teams, organizational groups (e.g. engineering, marketing), and coordination (leadership).

Becoming a SPoF can arise from a variety of ways:

- Using a language of framework that only you understand
- Being the only one with access to deploy code, modify a database, access an admin panel, etc.
- Writing non-obvious code with no documentation
- ... and many more

SPoFs become massive problems during the worst times.

Imagine having downtime because of a bug in the code, and your entire team (except you) is rushing to figure out how the code even works.
Hours later, they finally sort out the issue (or have some temporary workaround), but can't deploy the fix because they need your explicit approval in Github for the CI/CD to run, and nobody has direct access to Kubernetes.

It means that the downtime of the entire organization = your downtime, and humans are not highly available systems.

While this can be compensated for by [being available](#availability), as we say in distributed systems "2 is 1 and 1 is none".

It's actually quite trivial to avoid being a SPoF:

- Choose languages, frameworks, and tools that your team is familiar in. If not possible, educate your team on what's new (and why)
- Never have sole access to make changes to code, infrastructure, files, or internal tooling
- Write really good docs. So good that someone could understand how the system works without looking at a single line of code (just reading docs). Or "good enough that a dumb LLM could contribute".
  - For higher-level architectural docs, write great markdown files, diagrams, or explainer videos
- **Educate your team such that you could vanish tomorrow without hard-stopping your organization.**

## Always seek to get better, and are not offended

> _Deciding that you are done learning is deciding that you are done progressing in life._
>
> _Exceptional people never put down the desire to learn more, to be better at what they do._
>
> _When mistakes are made, whether collective or individual, they do not take offense, bur rather seek to understand how they could improve or prevent the mistake in the future. They don't become defensive, they become open to feedback and understanding._

The saying "you become the average of the N people around you" really is true.

People who have given up on learning have this "social stench" to them. They consume more than the produce, they become complacent and roll over when things get hard.

They've effectively given up. They've capped their value to their team, their family, and their society.

Don't do this to your team, exceptional people always seek to understand more.

They seek to get better at what they are great at, improve upon their mistakes, and explore new practices and technologies whether it enhances their life or just their familiarity with more of the world around them.

They don't think "I know so little" or "I'm so bad", they think "I have so much to learn" and "It's proven I can be so much better".

The present was not built by people who decided that we didn't need anything more.

Exceptional people recognize the potential to be better, to know more, and to do what others won't.

It makes sense that to get better compensation, that should be derived from being better than your were before?

### Always open to changing your mind

> _Exceptional people know when they're wrong, and change their minds easily._
>
> _When they believe others are wrong, they explain why to educate, not criticize._

There's nothing impressive about dying on the wrong hill, especially when you know it's wrong, and have no validation otherwise.

Exceptional people quickly recognize when their understanding or beliefs are wrong, and quickly adjust course.

They're not afraid to say "I was wrong".

They're not afraid after 30 minutes of debating to say, "you know what, I think I was wrong, I'm with you now".

They NEVER say "I think you're wrong.", they always explain why "... because xyz".

A statement without evidence is just an opinion, not a fact.

They recognize that people have a tendency to dig deeper into their holes during conflict, rather than rationalize whether it's the right hole to dig. They keep this natural tendency at the forefront of debate to ensure they avoid it.

## Think like your users

> _Exceptional people always consider who they are building for._
>
> _If they're not thinking from the mindset of their users, they're thinking from the wrong mindset._
>
> _If they're not testing it how their users would interact with it, they're testing it wrong._

It's pretty simple.

Either you're building for your users, or you're building for yourself. The former is correct, the later is detrimental.

This goes for understanding why to make something, sculpting it for the user, and ensuring that it's tested like them.

Often in testing, you'll find issues that you didn't think of during the building process. The UX might suck, edge cases you didn't consider, etc.

That's typically always going to happen, and it happens because you build from the opposite side that it's used from.

## Understanding why

> _Understanding why something is being done is almost always as important as doing it in the first place._
>
> _Exceptional people don't blindly add features, design interfaces, rearchitect the backend, etc._
>
> _They seek to fully understand why a decision has been made to do this, giving them empathy for the end user or system. They look at other implementations and alternatives, and seek the decision process and reception of that implementation to better inform the creation of their own._

Seeking an understanding of why something is being done is a standard in exceptionality.

A designer will seek to understand why an interface is being made, enabling them to recognize faults in UX. They will look at how something has been done on other products, looking for ways that it could be better, or common mistakes that other products implement.

An engineer will seek to understand why a feature is being implemented, so as they're testing it they can get a good feel whether the user might like it, surfacing concerns before it gets deployed to end users. They look to understand why a certain architecture is being used over another one they're familiar with, and can ask questions about how it handles certain scenarios, potentially revealing faults before they become downtime.

## Responsibility & ownership

> _Responsibility is something that is demonstrated, not awarded._
>
> _Responsibilities are given to responsible people._
>
> _People who have not proven themselves capable of more responsibilities are not given them._
>
> _Exceptional people exercise responsibility beyond their responsibilities, demonstrating that they are eligible to be given more responsibilities._
>
> _Being given responsibilities is being given ownership of a segment of the business._

Showing that you have the responsibility to have judgement and authority on key components of a business and team is a direct measure of an exceptional team member.

### Dependability

> _An exceptional team members gets done what they say they are going to get done._
>
> _Their dependability extends beyond any standard rails that the business operates on._

All that should be needed to know that someone is going to get something done is acknowledgement. Whether that's a ping in slack, or mentioning a task on a video call, they'll get it done.

They don't say, "ok can you make that an issue on Github for me?" or "make that a task?". Obviously if I had the time to do that, or I had the detail, I would have already. They make their own note, and chase it down with the appropriate urgency, adding it to Github or a task board if they feel the need.

They can be depended on for the output of their work: Their code is tested in prod, their spelling is checked, and

Exceptional people are dependable in information retention too.

They retain information from calls because they recognize the need to take notes. They know they can't hold more than a few details in memory as well as starting to ask questions, so they write down the key points.

### Availability

> _Being available for your team is being a team player. My offering minuscule amounts of time and attention from your otherwise off-hours, you prevent your prevent the scenario where your team loses the majority of theirs._
>
> _Being available to solve any critical issues that arise quickly brings immense value to the team, and stops compounding problems dead in their tracks._

Being available is crucial for many reasons:

- Unblocking team members (your #1 priority)
- Being available on weekends to answer questions, be pinged for downtime, etc.

That does not mean you have to answer any questions that someone drops for the next day, but it means having the discretion to know when you need to step in to action.

**Example scenario:**

1. Let's say some service has *stopped working*, and someone who is not super familiar with that service responds to a customer inquiry about it.
2. They immediately jump into action, but there's just too much detail to understand, so they ping you. Crickets.
3. They found out through trial and error that restarting the service restores it for a few hours, but then it stops working again.
4. The weekend has just begun.
5. Now they, potentially any other innocent team members that are roped in because they are available, are now playing restart hot-potato the entire weekend.
6. You come online Monday
7. You see the ping (because of good **Communication**), recognize the logical error, and find the fix is a 2-liner tweak in 15 minutes
8. Problem solved, but multiple members if your team had their weekends ruined.

**Let's see how being available fixes that:**

1. Let's say some service has *stopped working*, and someone who is not super familiar with that service responds to a customer inquiry about it.
2. They immediately jump into action, but there's just too much detail to understand, so they ping you.
3. You recognize the issue… 15-minute fix to start your Saturday
4. You and your entire team get their full weekend

Now it should be clear how being available to your team, even when you're not expected to be working, is being a team player.

I won't bother to explain the scenario of critical downtime, I'll just show you how the CEO of supabase, days after raising 200M on a 2B valuation, is available within 5 minutes of getting a ping on Bookface (YC's internal social media). *I'm not supposed to screenshot BF, but I think this is an ok exception.*

<img width="798" alt="image (1)" src="https://github.com/user-attachments/assets/703e4e43-c218-48e0-8559-a76b607ae2a6" />

From initial post to final comment was 7 minutes.

If someone like Paul Copplestone can be available on a Sunday evening for his customers that are working on a Sunday, demonstrating high **Agency** by coordinating immediate support for a critical issue for a customer, so can anyone else on the team.

Now that's a customer for life.

Everyone on the team should be held accountable for having high agency.

### Context discovery

> _Highly responsible people spend 15-45min to start their day by figuring out what happened while they were offline, or otherwise occupied._
>
> _They do this to gain context on what the rest of the team is doing and look for any mistakes or miscommunication._

Things happen when you are busy, not a problem.

Not finding out *what happened* when you were busy, that's a problem.

Sometimes you are pinged on those things, and you should be aware of them like previously mentioned.

Sometimes you are not, but the act of collecting the context of what happened while you were offline (or otherwise distracted working) is an important trait for responsible teammates.

**Example**:

1. While you're offline, there's some downtime. You're not on call, so you're not pinged
2. The on-call engineers handle the situation, but do so by implementing a new correctness bug that you would have spotted immediately from the slack conversation
3. You *don't* read the downtime thread when you come online
4. … days go by, logs are leaving their retention, hundreds of thousands of calls are happening
5. Customer says "hey I was reviewing my calls from last month and I noticed X, this is wrong"
6. Over the new few hours, the issue is escalated up to top management because of the severity of how badly this messed up not only one customer, but *all of them*
7. Logs have been discarded, cannot use logs to recover all the issues
8. *Major business damage, major relationship damage*

**Let's modify the example for a responsible team member who reviews all possible relevant slack threads when they come online:**

1. While you're offline, there's some downtime. You're not on call, so you're not pinged
2. The on-call engineers handle the situation, but do so by implementing a new correctness bug that you would have spotted immediately from the slack conversation
3. You come online, and start your day by reading through all the slack threads in your relevant slack channels before you start your day
4. You come across the downtime and give a little more attention when reading through this thread
5. You glance at the PR that was implemented to fix the bug, uh oh, that's wrong!
6. You immediately ping the team that implemented it, explaining the issue, and within 30 minutes of you coming online (say net +7 hours after the bug was introduced) the bug is fixed. Luckily, since calls don't really happen over night, only a handful were impacted, and can be manually adjusted from the logs of the previous hours

### Miscommunication hedging

> _Being a good communicator means communicating clearly, communicating concisely, and hedging against communication faults (like missed pings)._
>
> _For every channel that you are expected to be reachable on (e.g. slack), you check your mentions to start your day, when you come back from lunch, 1hr before you end your day._
>
> _You seek clarity when things are potentially ambiguous or changing._

Sometimes communication issues happen:

1. Your phone doesn't get a ping
2. You open a notification, tell yourself you'll address it in 5min after this code is pushed, and your forget

etc.

This can *trivially* be hedged against with a few things that take at most minutes of your day. This prevents small miscommunication from becoming a massive lapse in team performance and reliability. "Oh I missed your ping" +14 hours later when the person sends "@you ping" is another way of saying "I'm not taking a few minutes of my day to prevent 10+ hour spins on productivity for my team".

Sometimes you haven't addressed it yet because there were higher priority things to attend to. Good. But you marked it down such that you've not just lost the ping, you're guaranteed to get back to it at some point, because you were **Responsible** in keeping track of communication.

### Use AI Often But Responsibly

> _Exceptional people supplement their knowledge and expertise with AI, they don't replace it._
>
> _They take full agency to give it the best possible context, verify output correctness, quality, and take full responsibility for what ever it does._

LLMs and agents are amazing, but they are not a silver bullet.

They hallucinate, they sometimes are comically dumb, and almost always lack massive amounts of critical context.

Yet despite that, exceptional people know how to use it to their advantage.

They:

- Ask thinking models loaded with the appropriate context to confirm their understanding, and don't take the answer as the necessary truth
- Review *everything they do*, taking full responsibility for everything they ask an LLM or agent to do
- Find ways that AI can help, not bloat
- Gut-check with it constantly as an opportunity to correct misunderstanding, not validate their understanding (which it hallucinates often). They don't fall victim to hallucinations, they always verify.
- Understand how to provide it with the proper context to give it the best chance possible to give useful (and correct) answers.

## Other Resources

Some other resources I think are great, and well written. Linking them directly both for credit, and also to keep this README from being _massive_.

- [Operating well - what I learned at Stripe](https://samgerstenzang.substack.com/p/operating-well-what-i-learned-at)
- [What I Miss About Working at Stripe](https://every.to/p/what-i-miss-about-working-at-stripe)
