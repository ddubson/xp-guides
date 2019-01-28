# Extreme Programming (XP)

- [Principles, Values, Practices](#principles-values-practices)
- [Why XP?](#why-xp)
- [What is XP?](#what-is-xp)
- [XP Values](#values)
- [Practices](#practices)
  - [Balanced Team](#balanced-team)
  - [Iteration Planning](#iteration-planning)
    - [Estimation](#estimation)
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

__Principles are domain-specific guidelines for life.__ [1]

__Values are the roots of the things we like and don't like
    in a situation.__ [1]

__Practices are evidence of values.__ [1]

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

__Stay aware. Adapt. Change.__ [1]

__You don't wait a long time to find out if you were going the wrong way.__ [1]

## Values

__Values bring purpose to practices__ [1]

Values drive practices.

The five core values of Extreme Programming are:

- Communication
- Feedback
- Simplicity
- Respect
- Courage

## Practices

### Balanced team

An autonomous team that has people with a variety of skills and perspectives
that work together towards a common goal.

### Iteration Planning

TBD

(Highest priority features first approach)

#### Estimation

TBD

Addresses Risks:

![Staff Turnover](https://img.shields.io/badge/Risk-Staff_Turnover-red.svg)

### Pair programming

![Communication](https://img.shields.io/badge/Value-Communication-brightgreen.svg)

![Communication](https://img.shields.io/badge/Value-Feedback-brightgreen.svg)

Programming practice in which two developers work on the same workstation
but with two monitors, keyboards, and mice and a mirrored display.

#### Ping-Pong Technique

Ping Pong pairing is the practice in which one developer writes a
failing test, and the pair writes the logic to make the test pass.
Once the test has passed, another test is written by the same person,
then the next person writes the logic for that failing test. And so forth.

#### Benefits of Pair Programming

- Diffusion of knowledge
- Cleaner and better designed code through lively discussion of patterns and
    techniques to use
- Better conversation about what is being built and what is needed and
    what is not.

### Test-Driven development

![Simplicity](https://img.shields.io/badge/Value-Simplicity-brightgreen.svg)

Test-driven development is an approach to software development in which for
any given slice of logic to be built in the software system, the test for that
logic is written first, and only then is the actual logic written to satisfy
the test case.

#### Run on every change

Tests that are written and made to pass, are thereafter run on every single
change to make sure that the system is as per specification.

Addresses Risks:

![System Goes Sour](https://img.shields.io/badge/Risk-System_Goes_Sour-red.svg)

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
    test in place, we might never know about it." [2]
- "We know that we should refactor it to make it more understandable, but then
    there is that issue of testing again. If we don’t have tests, how do we know
    that we are refactoring correctly?" -- [2]

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

### Technical retrospectives

To be able to learn effectively if a process or a technique is working or not,
it is important to hold technical retrospectives
(i.e. 'tech forums', 'techtros') to discuss and acknowledge winning
strategies and techniques, as well as things that are just not working
and should be scrapped.

This is also a place to perform show+tell by developers to showcase
some new and interesting things in the code that every one should be
on the same page about.

## References

1. [Extreme Programming Explained: Embrace Change (2nd Ed., 2004) -
    Cynthia Andres, Kent Beck](https://www.amazon.com/Extreme-Programming-Explained-Embrace-Change/dp/0321278658)
2. [Working Effectively with Legacy Code -
    Michael Feathers](https://www.amazon.com/Working-Effectively-Legacy-Michael-Feathers/dp/0131177052)
