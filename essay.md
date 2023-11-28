# Introduction

Responsible code development is not a byproduct of good programmers.
It is a paradigm of development in and of itself. It is this paradigm that shapes
the modern programmer, the weight on which it lays can be seen in the software issues of the past.
The Therac-25, a machine with software that had not been scrutinized, leading to deaths. The 2012 Knight Capital incident
leading to losses of millions because issues stemming from integrating changes into an old system. The Y2K incident
spreading panic among civilians based on the idea that the internal clocks of old systems would not be able to represent
the year 2000 causing system failures. All of these, are grounded on the limited role reliability played in past system development.
To meet these issues, we have shaped various procedures to underline our development. One of these is continuous integration.

When developer make rapid changes as they have to do during team development 
they inadvertently introduce many issues to the stability and quality of the shared code base.

Continuous integration is the process of enabling developers to still make rapid changes to an existing code base while sustaining
code reliability. This is done through two main strategy, the first is running tests on changes and the second is to, 
depending on the results of these tests control the actual changes made to the shared code base.

# The Tests

Poking holes in programs, observing if they fail allows us to find errors that otherwise would
have flown by our radar. Testing in software is a crucial part and one principle that is of especial
importance is brought up in an article on software testing, A test cannot prove the reliability of a program, it 
can only prove that lack of it.\cite{IEEE}

We must be wary, if we do not heed this, we may end up building and building without having ever broken the code down, 
leading to bugs that were once easy to catch, now, layered deep beneath mazes of functionality.

## Manual Tests A Review Approach

Manual tests is a valuable step of this process and, thus, a big focus of CI is enabling the
correct peer review system so that the quality of the code does not falter.

### The Power of the Mind
The mind of humans can do amazing things, a computer is good at running enormous amounts of
specific tasks but the mind is good at making connections. This is the power of the mind, our ability
to abstract and reason about code changes is invaluable and is something a computer cannot yet accomplish to the same proficiency.

### The Right Environment
However, the mind needs the right environment to do what we want properly, to avoid falling into
lazy habits such as just pressing 'okay' for an upcoming change. We have to shape the right kind of
environment that values feedback and discussion over conflict avoidance.

### How to Foster the Right Environment
To make the environment correct, we have to enable our creative and thinking part, we have
to make code reviewing into a problem solving activity instead of a defect finding venture.
This implies that changes are to be discussed, and we need tools that allow effective discussing of code. Thus, we are searching for tools for code referencing, response referencing and easy access to coworking sessions of visual demonstrations of issues. This allows the reviewer to easily reference and exemplify with visuals 
problems in the code and the author to effectively reference the reviewers' comments and edit in the visual diagram if necessary for clarification.  (cite VPS). Moreover, we are making the information into a much more compact form by diagramming instead of having a bunch of text describing the situation. This helps people hop on the review process that has already started.

### Selecting the Right Process
- The old code review process
    The older process consists of a methodical line by line inspection of code (cite Saner). This approach
    was very time consuming and, thus, was not practical enough to apply at companies.
- The Modern Code Review
    The modern process of code review is focused on small changes and fast interactions. (cite Saner) This brings up a very important connection to what the human mind is built for, we are good at reasoning and abstracting. Thus, if a change is made in the name of a specific process, instead of reading line by line we can focus on the abstract of how the new change is made possible by code. This means that for effective code reviews we should make sure that our changes standout. For example, using diff tools to highlight changed code but we should also make sure that the idea that the change addresses is discussed in the imported change. If the author tried to translate an idea into code, this should be relatively simple to address since the idea is what the author began with. (cite google research).
    Moreover, we need to realize that we are emotional creatures and studies have shown that negative feedback provide worse results. This means we have to focus on discussing the problems rather than the humans and if we decide to discuss the humans involved we should be focusing on positive aspects (cite google research).


## Automated Tests

However, if testing is only manual, then we are not leveraging the full capacity of the modern computer, a modern computer can run millions of tests and always remembers to rerun tests that we have written. Thus, we have the frameworks for breadth and the assurance of memory that we do not have with manual testing. It is essential to utilize these aspects of testing to catch bugs that are reflected in coding mistakes rather than in ideas and how they are supposed to be implemented and catch bugs that break parts that humans simply could not have noticed during a short inspection.


### The Smart Input Selection

### A modular approach
ModularizedTesting(1).png


## The Manual and Automatic Synergy

### Regression Tests

# The Control

## Version Control Systems

## The Feedback Control

# A worked example: Our Java Calculator

## The CI file

## A photo of test runs

## Control upon Merge and protected branch system

# Conclusion


