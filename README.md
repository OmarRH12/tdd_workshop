# Purpose
Dive deeply into TDD by sharing experience and practicing new tools
- Practical workshop, full of examples
- Thinking programming as communicating 
* Simple, clear, robust code
* Maintainable, scalable, undestandable
* Effective, resilient to change

# Persona
- Ada: A software developer in the beginning of a journey to become the best developer she can be. 
With a background in exact sciences, she has heard about tests but does not practice TDD.
She has some software patterns in mind from recent learning, but limited experience in structuring code.

# Disclaimer
Sharing is caring! This is part of a learning journey. I am much more a curious individual than an expert. The objective is to share my learnings so far while enabling us to collaborate, learn and connect around an important topic. I assume that independently of your experience, you are curious to learn, courageous to ask and share and, finally, respectfull about the stage each one is right now.

# Community
In Slack: #tdd-test-driven-development.

# Requirements
- Installed VSC
- Installed python version
- git
- github account with Equinor
- Camera
- Formatting tool: black (we will talk about it ;-) )

# Story

Warning: the workshop is based on our own work together. You may find imperfection or questionable things. Follow up and raise hand to ask and help!

We will go through:
1. Check that all requirements are in place for all
1. Have a short pause (eventual catch-up with missing requiments)
1. Present a problem to solve
1. Demonstrate TDD while working together (~peer-programming)
1. After each step, a pause for:
    - sharing the work
    - discussing key topics/challenges
    - catching up (or pull from a repository)
1. Conclude with a recap, references for further learning

Commit early and often!

## 1. Does everyone have the requirements?
- VSC: terminal type "code" and VSC should open
- python --version 
- git --version, black --version
- github: clone repository locally (where Github Actions is setup)
- Have a recipe: Create a virtual environment and configure in VSC
- Have a recipe: Clone, SHA, git pull, git branch, git add, git commit, git push


## 1. The problem: String calculator¹

### Step 1:

The method can take up to two numbers, separated by commas, and will return their sum.
For example "" or "1" or "1,2" as inputs.
For an empty string it will return 0.

The cycle is as follows:
0. Make a list of tests we know we need to have working
1. Add a little test: write just enough of a test to fail
1. Run all tests and fail
1. Make a little change: write just enough code to make it pass
1. Run the tests and succeed
1. Refactor to remove duplication: clean up the mess made getting the test to pass

Discussion:
- Being able to take teeny-tiny steps, not necessarily doing it
- Add items to our to-do list rather than addressing them all at once
- Commit early and often!
- Let's try: Test pipeline, continuous integration
- Remember to save changes :-) 
- DRY: Don't Repeat Yourself!
- Debugging with test (tools?)

### Step 2
Allow the Add method to handle an unknown amount of numbers.

### Step 3
Allow the Add method to handle new lines between numbers (instead of commas):
- The following input is ok: “1\n2,3” (will equal 6)
- The following input is NOT ok: “1,\n” (not need to prove it - just clarifying)

### Step 4
Surprise!

# Conclusion
- What was useful?
- What was not?
- Let's try: Test pipeline, continuous integration
- Remember to save changes :-) 
- DRY: Don't Repeat Yourself!

# Testing

1. Why should we test? 
    - Intention of code, documentation coverage (in/out), confidence (failing test)
    - Bugg (regression test)
    - Refactoring (know the desided behaviour)
    - Using testing to review
1. TDD:
- avoid spaguetti code
- if it is hard to write a test: think about what you are trying to code
- side effects (non obvious behaviour/not main goal)
1. Continuous integration
- Test in Github actions (or Circle CI, Jenkins)
- Features: scalable 

# Additional resources
- TDD chanel

# Contributors
Grateful to colleagues contributing behind the scenes:
- LauraSManns 
- lars-petter-hauge
- oyvindeide
- Lars Kåre

# References:
¹ https://kata-log.rocks/string-calculator-kata
