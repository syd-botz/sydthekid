---
title: "[dev shit] may you always unblock yourself: a few problem solving techniques"
date: 2020-11-05T13:45:08-06:00
showDate: true
---

as an everything-feels-new software developer, i return to this list of questions OFTEN when i am just completely stuck or even during the thousand 
moments during a day when i am just trying to figure out what the next step should be. i developed this list of questions during my first
professional experience as a software developer with my tech lead, Karan Krishnani. 

i am a firm believer that one of the most important parts of being a good software developer (and maybe just being good at anything...lmk your thoughts on that) is 
knowing how to ask the right questions and figure out what you don't know. enjoy and happy problem solving!

## When I don’t know what is going on …

- Have I proved to myself where my problem is stemming from? If not, how can I increase my confidence in the place to begin debugging?
    - Logging, more research, more manual testing, etc...
    - Am just assuming that I understand what and where the problem is stemming from? (THIS IS SO IMPORTANT.)
- What kind of logging will help me learn more about what I do not know?
- How consistently can I replicate the issue?
- What do I expect to happen when I do “x”?
- Which environment is the problem happening in? If the probelm is in a CI, staging, or production environment, am I able to replicate the problem in my local environment to decrease the feedback loop? What are the differences between the environment on which this works vs the environment on which it doesn’t?
- Can I use a sandboxed environment (like [CodeSandbox](https://codesandbox.io/)) to simplify the problem and gain a deeper understanding of the problem at hand? 
    - This works particularly well if I am having trouble implementing details of a particular technology (ex: a new Material UI component) and I can use the sandbox to isolate what is new/broken
- Is there a point in the code that I can roll back my changes to and then incrementally move forward to figure out where “things went wrong”?

## When I understand the problem and I’ve tried to fix it in many ways...

- What does the appropriate documentation have to say about the problem at hand? When was the last time I read the documentation?
- Have I looked into other packages or another syntax that will more simply and elegantly do the same thing that is blocking me?
- What is the big picture problem I am trying to solve? Am I actually solving this problem or am I solving a subproblem of this? Can I try to solve a different subproblem that will unblock me and move me close to the final goal?

## When I am trying to understand where I am stuck...

- Do I have a lack of technical domain expertise that is holding me back? Where can I gain that expertise?
- Am I experiencing unexpected or unexplainable behavior? What steps can I take to illuminate more about why a particular thing is happening?
- Is a 3rd party package or dependency behaving unexpectedly (aka there is a bug) or is the problem in my own use of that dependency? Do I need to abandon this package? What would convince me that this package is worth fixing this issue or worth abandoning?
- Do I indeed understand the problem but I am blocked because I do not know how to solve it?
- Am I overwhelmed by the number of technical solutions? What kind of questions should I be asking myself about possible solutions that will help me make the best decision? What are the most important thing(s) I need a solution to do/be? Can I create a document or spreadsheet to help narrow down the possible approaches?

## When I am considering involving other people...

- Do I need to involve other team members in making a technical choice that has particular consequences?
- Have I asked myself the above questions and can articulate where I am blocked to someone who can help me?

## While solving a problem generally…

- Have I been making small changes and testing them individually? Fail fast! Do I understand why I made each change and the behavior that followed?
- Once I have the correct expected behavior, can I thoroughly explain what the solution was? If not, what parts still confuse me?
- Is there "bad data" involved? Have I traced the code to see where a bad input is coming from? Have I traced the code to see why this function is even being called? Have I traced the entire data flow / application flow to gain an understanding of the codebase?
- Should I use any external tool to help me diagnose the issue?
    - Database query tool (ex: [pgAdmin](https://www.pgadmin.org/), [dBeaver](https://dbeaver.io/))
    - SSHing into higher environments (ex: Heroku Run Console)
    - Checking logging on higher environments (ex: [Papertrail](https://www.papertrail.com/))
    - Package specific browser dev tools (ex: [Redux DevTools](https://chrome.google.com/webstore/detail/redux-devtools/lmhkpmbekcpmknklioeibfkpmmfibljd), [React Dev Tools](https://chrome.google.com/webstore/detail/react-developer-tools/fmkadmapgofadopljbjfkapdkoienihi?hl=en))