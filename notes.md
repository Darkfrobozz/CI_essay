We will divide CI into two concepts:

# Tests
    There are many ways to test a program, tests are what makes modern continuous integration.
    For example, we cannot assure that all small changes due not cause some catastrophic change if we do
    not test it and we have manual vs automatic tests.

https://ieeexplore.ieee.org/abstract/document/4597151#:~:text=The%20principles%20that%20follow%20emerged,0814

## Principles
    - To test a program is to try and make it fail - not to assure quality, we are poking holes in an endless ocean
    - Tests are no substitute for specs - tests are by nature not general
    - Regression testing - turning failures into tests
    - Applying oracles
    - Manual and automatic testing
    - Empirical assessment of testing strategies.
    - A test's most important property is the number of faults it uncovers as a function of time

## Quotes
Impact of CI on code reviews:
https://cmustrudel.github.io/papers/cassee20saner.pdf
"Indeed, we find that on average the amount of discussion
during pull request reviews, operationalized in multiple ways,
decreases over time after the introduction of CI. At the same
time, we find that this decrease in discussion effort cannot be
explained by a decrease in expected pull request updates after
review—the number of subsequent pull request commits after
the pull request has been opened is, on average, unaffected
by the adoption of CI. Based on our models, we estimate
that on average CI saves up to one review comment per pull
request, giving rise to the idea of continuous integration as a
silent helper, where some of the tasks traditionally executed
by human reviewers are now carried out by CI."

"The notion of code inspections to improve
software quality was introduced by Fagan in 1976 [24]. Fagan
describes a process of line-by-line inspection of source code
during team-wide meetings. While this method has proven
to be effective [25], [26], it requires a significant amount of
human effort, hindering its adoption" (cite Saner)

The modern code review:
https://storage.googleapis.com/pub-tools-public-publication-data/pdf/80735342aebcbfc8af4878373f842c25323cb985.pdf

Code inspections:
Code Inspections. Software inspections are one of the first
formalized processes for code review. This highly structured

Asynchronous review via email. Until the late 2000s, most
large OSS projects adopted a form of remote, asynchronous
reviews

Tool-based review. To bring structure to the process of re-
viewing patches, several tools emerged in OSS and industrial
settings.

id Convergent Practice
CP1 Contemporary peer review follows a lightweight,
flexible process
CP2 Reviews happen early (before a change is commit-
ted), quickly, and frequently
CP3 Change sizes are small
CP4 Two reviewers find an optimal number of defects
CP5 Review has changed from a defect finding activity
to a group problem solving activity

The google approach:
Number of reviewers:
"Number of reviewers and comments. The optimal number
of reviewers has been controversial among researchers, even in
the deeply investigated code inspections [37]. Rigby and Bird
investigated whether the considered projects converged to a
similar number of involved reviewers. They found this number
to be two, remarkably regardless of whether the reviewers
were explicitly invited (such as in Microsoft projects, who
invited a median of up to 4 reviewers) or whether the change
was openly broadcasted for review [33].
At Google, by contrast, fewer than 25% of changes have more
than one reviewer,1 and over 99% have at most five reviewers
with a median reviewer count of 1. Larger changes tend to
have more reviewers on average. However, even very large
changes on average require fewer than two reviewers.
Rigby and Bird also found a “minimal increase in the number
of comments about the change when more [than 2] reviewers
were active” [33], and concluded that two reviewers find
an optimal number of defects. At Google, the situation is
different: A greater number of reviewers results in a greater
average number of comments on a change. Moreover, the
average number of comments per change grows with the
number of lines changed, reaching a peak of 12.5 comments
per change for changes of about 1250 lines. Changes larger
than this often contain auto-generated code or large deletions,
resulting in a lower average number of comments"
This suggests that we should require 1 - 2 reviewers for a code change.

Tone mindset:
"Interviewees perceive the communication
within code review as possibily leading to problems from two
aspects: tone and power. Tone refers to the fact that some-
times authors are sensitive to review comments; sentiment
analysis on comments has provided evidence that comments
with negative tone are less likely to be useful [11]. Power
refers to using the code review process to induce another
person to change their behavior; for example, dragging out
reviews or withholding approvals. Issues with tone or power
in reviews can make developers uncomfortable or frustrated
with the review process"
This suggests that we should not be focusing too much on the individual writing, but if we
do name anything about the individual (making it personal), we should keep it positive.

"Previous studies have found that the number of
useful comments decreases [ 11, 14] and the review latency
increases [8, 24] as the size of the change increases."
This suggest we should be reviewing small changes, which means we should be making frequent requests to merge
our code.

https://nfb.org/images/nfb/publications/jbir/jbir21/jbir110102.html
VPS Problems solving using visuals

## Review Testing
Manual tests is a valuable step of this process and, thus, a big focus of CI is enabling the
correct peer review system so that the quality of the code does not falter.
    - The Power of the Mind
        - The mind of humans can do amazing things, a computer is good at running enormous amounts of
            specific tasks but the mind is good at making connections. This is the power of the mind, our ability
            to abstract and reason about code changes is invaluable and is something a computer cannot yet accomplish to the same proficiency.
    - The Right Environment
        - However, the mind needs the right environment to do what we want properly, to avoid falling into
            lazy habits such as just pressing 'okay' for an upcoming change. We have to shape the right kind of
            environment that values feedback and discussion over conflict avoidance.
    - How to Foster the Right Environment
        - To make the environment correct, we have to enable our creative and thinking part, we have
            to make code reviewing into a problem solving activity instead of a defect finding venture.
            This implies that changes are to be discussed, and we need tools that allow effective discussing of code. Thus, we are searching for tools for code referencing, response referencing and easy access to coworking sessions of visual demonstrations of issues. This allows the reviewer to easily reference and exemplify with visuals problems in the code and the author to effectivly reference the reviewers comments and edit in the visual diagram if necessary for clarification.  (cite VPS). Moreover, we are making the information into a much more compact form by diagramming instead of having a bunch of text describing the situation. This helps people hop on the review process that has already started.
    - Selecting the Right Process
        The old code review process
            The older process consists of a methodical line by line inspection of code (cite Saner). This approach
            was very time consuming and, thus, was not practical enough to apply at companies.
        The Modern Code Review
            The modern process of code review is focused on small changes and fast interactions. (cite Saner) This brings up a very important connection to what the human mind is built for, we are good at reasoning and abstracting. Thus, if a change is made in the name of a specific process, instead of reading line by line we can focus on the abstract of how the new change is made possible by code. This means that for effective code reviews we should make sure that our changes standout. For example, using diff tools to highlight changed code but we should also make sure that the idea that the change addresses is discussed in the imported change. If the author tried to translate an idea into code, this should be relatively simple to address since the idea is what the author began with. (cite google research).
            Moreover, we need to realize that we are emotional creatures and studies have shown that negative feedback provide worse results. This means we have to focus on discussing the problems rather than the humans and if we decide to discuss the humans involved we should be focusing on positive aspects (cite google research).


## Automatic Tests
However, if testing is only manual, then we are not leveraging the full capacity of the modern computer, a modern computer can run millions of tests and always remembers to rerun tests that we have written. Thus, we have the frameworks for breadth and the assurance of memory that we do not have with manual testing. It is essential to utilize these aspects of testing to catch bugs that are reflected in coding mistakes rather than in ideas and how they are supposed to be implemented and catch bugs that break parts that humans simply could not have noticed during a short inspection.
    - Regression - fixing bugs, keeping existing functionality, testing updates
        Making sure new functionality does not break old functionality
        Regression tests as a mindset.
    - Property-based - testing a property of a testing. Using jqwik I can use it as a resource as well, (the website).
A quality program fosters cohesion and decoupling, This can be solved for larger programs by letting them be modular. This modular design also effects our tests as can be seen in the diagram below:
### Using a Picture for these 
    - Unit tests - testing individual components
    - Integration - testing components in relation to each other
    - System Tests - testing all components in union

# Work control
    There are ways to organize our work flow such that we can effectively use continuous integration.
    For example, having a feature and main branch where any merges are controlled by our tests.
    Here the notion of branch protection comes in.

# A Worked Example and Selecting Appropriate Tools