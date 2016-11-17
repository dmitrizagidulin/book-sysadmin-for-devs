# Introduction

Starting out as a developer, I had the typical "throw it over the wall"
mentality with regards to the general area of system administration, ops and
deployment. *My* job was to write application code. You know, the important
stuff. How it actually *ran*, how it was built and packaged and deployed (and
logged, and monitored, and so on), was *not my problem*. Devs who work for any
but the smallest companies often have this luxury - you write some code, it
passes the automated test suite (you *do* have one, don't you?) and (if you're
lucky and your company is smart) the human QA process, and then you can just
throw it over the wall to whatever combination of system administrators, DBAs,
devops team members, or even other more experienced developers, to actually
deploy into production.

This attitude is bullshit. As a developer, it is in your best interest to at
least have a vague idea of how the sausage is made, so to speak, of what is
involved in provisioning, deploying and scaling production systems.

As time goes on, and as Continuous Integration and Continuous Deployment ideas
and tools make their way into the dev mainstream collective subconscious, many
of these ops/sysadmin tasks get automated, and rightly so. But regardless of the
level of automation, human attention and expertise is needed to provision and
deploy most systems (or at least troubleshoot them when something inevitably
breaks).

I am *not* saying that everybody should know everything, or that system
administration and devops is so easy that there is no point in specialists
(because *any* developer should be able to do it). There are good reasons for
specialization, and most system administrators are worth their weight in gold.
Instead, the main point of this book is that system administration is very
important and relevant to application developers, but there are a lot of things
in that area that we don't get taught.

Why you should have a basic grasp of system administration, as developers:

- control the means of production
- it's great to know this stuff if you're an indie developer or if you want to
  deploy your personal projects
- reduce the time to deployment of prototypes
- knowing some of this stuff will give you more understanding (and, dare I say
  it, more empathy?) of what the ops teams have to deal with, and will make you
  better team members overall

## Audience

- mainly unix (linux) developers working with free or open source platforms
- mostly geared towards developers of web applications, web services or APIs
