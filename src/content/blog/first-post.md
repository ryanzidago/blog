---
title: "What I've learned building a resume builder"
description: "What I've learned building a resume builder"
pubDate: '2023-11-04'
---

Lately, I have been busy building <a href="https://coverly.vercel.app" target="_blank">Coverly</a>, a resume builder created with TypeScript, NextJS, TailwindCSS, Prisma, PostgreSQL and Vercel.

This has been quite the experience, with many rough edges along the way. Working on this project made me realize that there are many areas where I need to drastically improve if I want to continue to ship side projects! Which is a good thing because now I know exactly what to work on and how to improve. 

I have been working on it since March 2023, yet the outcome feels pretty thin. This is because:
- I wrote a V1 of the resume builder
- I wrote a code prototype for an onboarding experience à la TypeForm
- I wrote an application tracker where users could drag and drop applications across the pipeline
- I wrote a V2 of the resume builder because I wasn't that satisfied with V1

At the end of the day, only the last point is part of the final outcome!

Over the course of this project, I learned three things:
1. The importance of product research and prototyping before writing any line of code 
2. The importance of project management
3. The importance of setting a unique goal and sticking to it


## 1. The importance of product research and prototyping before writing any line of code

Spending more time observing what other resume builders were doing would have given me a clearer sense of what I wanted the end project to look like. 

At the beginning, I wasted some time making the resume work out of a JSON file as a database. It would have been better to use a real database first. 

Spending more time on how the user will interact with the form would have made it easier for me to implement it. 

Prototyping in code is more time-consuming than prototyping on a piece of paper or using an online sketch tool (Excalidraw). 

##  2. The importance of project management

At the beginning, I did not use a project management tool to create tasks and move them across stages as I was working on them.

I believe this to be a mistake. I have very little time to work on the project, so I need to work efficiently. Not only that, but I used to start working on a feature, then get distracted by another bug to fix or another feature that I deemed more important ...

Later, I added a project management tool (Todoist), and just writing down a list of the tasks to complete helped get them out of my head -- free some cognitive load. It also made prioritization way easier. 

## 3. The importance of setting a unique goal and sticking to it

This is the last point but the most important one. 

Retrospectively, I can say that I did not have a clear, unique goal of what I wanted to achieve when I started this project, even though I thought I did. 

I realize now that when I have so little free time, I need to be completely honest with myself as to what my goal is:
- Do I want to learn a new tech stack? If yes, am I willing to hack around to make it work? 
- Do I want to increase my attractiveness on the job market? 
- Do I want to learn how to design and build UI components? 
- Do I want to build a product and put it very quickly in the hands of customers? 

I told myself that my goal was to create a resume builder BECAUSE it would make updating resumes a more convenient experience, and I could do it using TypeScript, ReactJS, NextJS, Prisma BECAUSE I wanted to expand my knowledge and be more desirable on the job market, and I could learn a bit of UI design by building my own UI component, etc.

This is way too much. At the end of the day, I spent so much time trying to make the tech stack work together and hack around instead of building and shipping features (which I realized midway through was what I cared about the most). 

There's quite a cost to learning a new tech stack as a solo, part-time project builder:
- Vercel introducing breaking changes in NextJS 13 incompatible with NextJS 12, which is the version used for most tutorials you can find online. Now those tutorials are absolute, so you need to hack around to make it work, hunt for GitHub issue threads, or watch YouTube videos on how to use this app 
-  Being confused by the recent "React paradigm shift" being pushed by Vercel/NextJS where most of the code is rendered on the server by default while most React and NextJS tutorials use client side rendering ... 
- Learning a new ORM - Prisma - and discovering midway that it doesn't support polymorphism out of the box (unlike Ecto in Elixir).
- Realising that you can use Prisma generated types from your database model instead of writing your own type - but Prisma generated types don't include the model's associations, so now you actually need to write your own types that extend Prisma's types ... 
- Realising that Prisma consumes too many database connections due to a bug in how it's instantiated
- And so much more

All of those points above do not help me push more and better features. They do not directly contribute to the success of my project; they are just obstacles, distractions, and problems that I needed to overcome, ignore, or solve along the way without them benefiting my project. 

## Conclusion

Part of me wanted to give up along the way, but I decided that I needed to "suffer the full consequence of my decision", so next time I would be way more thoughtful in how I approach building a project, as I know I will commit until the end of it. 

I'm glad I went through it, learned that I need to be hyper-focused on one single goal, and can't wait to build the next project.


