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

Using this principle, when discussing testing we should focus our attention on trying to break our software. When
testing we want to break the software when writing we want to mend it to make it strong. One could make an analogy to muscles
tearing down to build back up stronger, this kind of process is what we are looking for. 

We must be wary, if we do not heed this, we may end up building and building without having ever broken the code down, 
leading to bugs that were once easy to catch, now, layered deep beneath mazes of functionality.

## Manual Tests A Review Approach

The power of the mind.

The necessary environment.

## Automated Tests A Modular approach

### The Smart Input Selection


ModularizedTesting(1).png
### Unit Tests

### Integration Tests

### System Tests

## The Manual and Automatic Synergy

### Regression Tests

# The Control

## Version Control Systems

## The Feedback Control

# A worked example: Our Java Calculator

## The Parser

## The AST

## Test Suites

## Control upon Merge

# Conclusion


