# Extreme Programming (XP)

- [Principles, Values, Practices](#principles-values-practices)
- [Why XP?](#why-xp)
- [What is XP?](#what-is-xp)
- [XP Values](#xp-values)
  - [Communication](#communication)
  - [Feedback](#feedback)
  - [Simplicity](#simplicity)
  - [Respect](#respect)
  - [Courage](#courage)
- [XP Principles](#xp-principles)
- [Practices](#practices)
  - [Sit Together](#sit-together)
  - [Whole Team](#whole-team)
  - [Balanced Team](#balanced-team)
  - [Iteration Planning](#iteration-planning)
    - [Estimation](#estimation)
  - [Weekly Cycle](#weekly-cycle)
  - [Pair Programming](#pair-programming)
    - [Ping-Pong Technique](#ping-pong-technique)
    - [Benefits of PP](#benefits-of-pair-programming)
  - [TDD](#test-driven-development)
    - [Red-Green-Refactor](#red-green-refactor-loop)
    - [Spiking](#spiking)
    - [Benefits of TDD](#benefits-of-tdd)
  - [Releases](#releases)
    - [Short release cycles](#short-release-cycles)
  - [Technical Retrospectives](#technical-retrospectives)

## Principles, Values, Practices

__Principles are domain-specific guidelines for life.__ [Source][1]

__Values are the roots of the things we like and don't like
    in a situation.__ [Source][1]

__Practices are evidence of values.__ [Source][1]

## Why XP

Software development involves a great amount of **RISK** in various forms:

- **Schedule slippage** - deadline is not met, and customers are not happy
    because they have to wait!
- **Project cancelled** - the software never makes it to production due
    to too many delays or other factors.
- **System goes sour** - system is put into production, but after some time,
    the cost of making changes or number of bugs (defect rate) rises to the
    point of the system needing to be replaced.
- **Defect rate** - software is put into production, but it isn't used due
    to the defects
- **Business misunderstood** - software is put into production, but it does not
    solve the business problem proposed originally.
- **Business changes** - software into production, but business problem it was
    designed to solve was replaced by another more pressing problem.
- **False feature rich** - lots of features, but none that provide actual
    customer value.
- **Staff turnover** - developers leave the project, potentially because of
    the underlying issues in the software.

XP seeks to address each of the risks outlined above, and will be described below.

> **When should I use XP?**
>
> When requirements are vague or change frequently.

## What is XP

XP is a software development discipline that addresses risk at all levels of the
development process.

__Stay aware. Adapt. Change.__ [Source][1]

__You don't wait a long time to find out if you were going the wrong way.__ [Source][1]

## XP Values

__Values bring purpose to practices__ [Source][1]

Values drive practices.

### Communication

Communication is integral to creating cooperation and a sense of team

### Feedback

__The sooner you know, the sooner you can adapt__ [Source][1]

### Simplicity

"What is the simplest thing that could possibly work?"

Communication helps achieve greater simplicity by introducing clarifications and eliminating any
unnecessary work.

### Respect

Respect the project and each other. If not, nothing can save the project from its demise.

### Courage

__The courage to speak truths, pleasant or unpleasant, fosters communication and trust__ [Source][1]

## XP Principles

- **Humanity** - software is developed by humans. To thrive, humans need:
  - Safety - from hunger, harm, threats. Loss of job included.
  - Accomplishment - opportunity and ability to contribute to society
  - Belonging - receive validation from a group they identify with
  - Growth - expanding skills and perspective
  - Intimacy - ability to understand and be understood by others 
- **Economics** - software must have business value, deliver on business needs
- **Mutual Benefit** - maintaining working relationships is paramount. Practices that
    benefit me now, later, and customers as well.
- **Self-similarity** - copying the structure of one solution into a new context, even
    at different scales.
- **Improvement** - nothing is perfect, but you can perfect your process, design, stories.
- **Diversity** - teams need differing skills, attitudes, perspectives to see problems
    in a different light, offering differing solutions
- **Reflection** - teams reflect and analyze what went right, what went wrong to
    see if they've succeeded, failed, or learned something new.
- **Flow** - delivering a steady flow of valuable software by engaging in all the
    activities of development simultaneously.
- **Opportunity** - problems need to turn into opportunities for learning and improvement.
- **Redundancy** - critical, difficult problems should be solved in several different ways.
- **Failure** - failure imparts knowledge
- **Quality** - making a big change efficiently in small, safe steps.
- **Baby Steps** - small, incremental steps over big changes all at once.
- **Accepted Responsibility** - responsibility is accepted, not assigned.

## Practices

### Sit Together

As a team, best results and outcomes from being within close proximity to each
other so that constant lines of communication are opened.

__the more face time you have, the more humane and productive the project__ [Source][1]

### Whole Team

Include all the team members to instill a sense of wholeness.

### Balanced team

An autonomous team that has people with a variety of skills and perspectives
that work together towards a common goal.

### Story Planning

Plan using units of customer-visible functionality

(Highest priority features first approach)

#### Estimation

Early estimation gives business and technical perspectives a chance to interact, creating
value early in the process to be able to estimate trajectory

Early estimation gets everyone to think about how to get the greatest return
from the smallest investment

Addresses Risks:

![Staff Turnover](https://img.shields.io/badge/Risk-Staff_Turnover-red.svg)

### Story Size

Make sure the stories written address the single smallest unit of value delivered to the
customer. The smaller the story, the easier it is to estimate, and deliver as compared
to larger stories, which can be inherently more complex.

### Slack

Include minor tasks that can be dropped if you fall behind schedule. Stories can be delivered
if you have additional time, or bumped over to the next cycle if no time
is left. This 'slack' can go a long way to boosting morale and defusing the pressure
that software teams have on delivering "the world" by a certain deadline.

### Pair programming

![Communication](https://img.shields.io/badge/Value-Communication-brightgreen.svg)
![Simplicity](https://img.shields.io/badge/Value-Simplicity-brightgreen.svg)
![Feedback](https://img.shields.io/badge/Value-Feedback-brightgreen.svg)
![Courage](https://img.shields.io/badge/Value-Courage-brightgreen.svg)

Programming practice in which two developers work on the same workstation
but with two monitors, keyboards, and mice and a mirrored display.

#### Ping-Pong Technique

Ping Pong pairing is the practice in which one developer writes a
failing test, and the pair writes the logic to make the test pass.
Once the test has passed, another test is written by the same person,
then the next person writes the logic for that failing test. And so forth.

#### Benefits of Pair Programming

- Keep each other on the task at hand
- Diffusion of knowledge
- Cleaner and better designed code through lively discussion of patterns and
    techniques to use
- Better conversation about what is being built and what is needed and
    what is not
- Hold each other accountable to team practices

### Weekly Cycle

Plan work one week at a time, utilizing [iteration planning](#iteration-planning)
to plan out a week's worth of stories, which can be assigned as stories get completed
by pairs of developers.

### Test-Driven development

![Simplicity](https://img.shields.io/badge/Value-Simplicity-brightgreen.svg)
![Feedback](https://img.shields.io/badge/Value-Feedback-brightgreen.svg)

Test-driven development is an approach to software development in which for
any given slice of logic to be built in the software system, the test for that
logic is written first, and only then is the actual logic written to satisfy
the test case.

Addresses:

- **Scope Creep** - explicit test cases drive the functionality that you're working on without
    letting scope extend past what you are working on
- **Coupling and cohesion** - test driving logic inherently creates a testable system which
    creates a well designed system that has low coupling, and high cohesion
- **Trust** - gives trust to other team members because everyone's written logic is tested
    and the fear of changing a piece of code is vastly reduced due to the tests in place.
- **Rhythm** - each step along the way in the story is much clearer with TDD since tests
    guide your progression and it is much easier to stick to the path to completion.

#### Run on every change

Tests that are written and made to pass, are thereafter run on every single
change to make sure that the system is as per specification.

#### Red-Green Refactor Loop

- A failing test is written first (RED)
- Logic is written to satisfy the condition under test (GREEN)
- If needed, improve code clarity, cleanliness, space or runtime complexity
    of logic (REFACTOR)

In the primary case, the 'happy path' of any given logic is written first.
Followed by additional edge cases or non-happy paths.

#### Spiking

If wading into territories that are unknown on how to approach writing a test,
it can be useful to 'spike', or build without tests, on a piece of logic to
gain an understanding of how it would conceptually work. Spiking is followed
by stepping back and, with the new understanding of a piece of logic,
following TDD to slowly introduce the logic into the system.

#### Benefits of TDD

- "A change in one place can affect behavior someplace else; unless we have a
    test in place, we might never know about it." [Source][2]
- "We know that we should refactor it to make it more understandable, but then
    there is that issue of testing again. If we don’t have tests, how do we know
    that we are refactoring correctly?" [Source][2]

Addresses Risks:

![System Goes Sour](https://img.shields.io/badge/Risk-System_Goes_Sour-red.svg)

### Releases

![Feedback](https://img.shields.io/badge/Value-Feedback-brightgreen.svg)

#### Short release cycles

Code that is checked in to the version control system should be built
(incuding running of tests, packaging, publishing artifacts) by a continuous
integration system, and deployed to a higher environment such as PCF.
This leads to being able to accept or reject user stories quickly and
effectively. In addition, it allows the stakeholders to review what's
been built, as well as ability to test the features built with potential users.

On every commit to `master`...

- Test
- Build
- Package
- Publish
- Deploy

Addresses Risks:

![Schedule Slippage](https://img.shields.io/badge/Risk-Schedule_Slippage-red.svg)
![Project Cancelled](https://img.shields.io/badge/Risk-Project_Cancelled-red.svg)
![Business Changes](https://img.shields.io/badge/Risk-Business_Changes-red.svg)

### Quick Builds (10-minute build rule)

Automatically build the whole system and run the tests in 10 minutes or less.

Longer builds tend to be avoided, defeating the purpose of having builds, and
undermining the value of Feedback.

### Continuous Integration

Integrate changes as they are completed, as early and often as possible to get feedback
as soon as possible on the health of the system, and the changes made in a story
that might have affected the overall system.

### Technical retrospectives

To be able to learn effectively if a process or a technique is working or not,
it is important to hold technical retrospectives
(i.e. 'tech forums', 'techtros') to discuss and acknowledge winning
strategies and techniques, as well as things that are just not working
and should be scrapped.

This is also a place to perform show+tell by developers to showcase
some new and interesting things in the code that every one should be
on the same page about.

---

[1]: https://www.amazon.com/Extreme-Programming-Explained-Embrace-Change/dp/0321278658 
    "Extreme Programming Explained: Embrace Change (2nd Ed., 2004) - Cynthia Andres, Kent Beck"
[2]: https://www.amazon.com/Working-Effectively-Legacy-Michael-Feathers/dp/0131177052 
    "Working Effectively with Legacy Code - Michael Feathers"
