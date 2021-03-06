# Contributing

External contributions are the best. Any feedback, bug reports and best of all pull requests would be greatly appreciated.

## Issue submission

Before submitting an issue please do the following:

* Make sure you're on the latest version `npm update -g generator-cardboard`
* Use the search feature to ensure that the bug hasn't been reported before
* Included as much information about the bug as possible, including any output you've received, what OS and version you're on, etc.
  
[Submit your issue](https://github.com/jeshuamaxey/generator-cardboard/issues/new)

## Quick Start

- Clone the repo of [generator-cardboard](https://github.com/jeshuamaxey/generator-cardboard), `cd` in and run `npm install`.
- Link it globally by running `npm link`, also from the root of the generator
- Run `yo` and you should now see the linked generators in the list.
- Start hacking :)

## Style Guide

This project uses single-quotes, two space indentation, multiple var statements and whitespace around arguments. Use a single space after keywords like `function`. Ex:

```
function () { ... }
function foo() { ... }
```

Please ensure any pull requests follow this closely. If you notice existing code which doesn't follow these practices, feel free to shout and we will address this.

## Pull Request Guidelines

* Please check to make sure that there aren't existing pull requests attempting to address the issue mentioned. We also recommend checking for issues related to the issue on the tracker, as a team member may be working on the issue in a branch or fork.
* Develop in a feature branch which was branched from the latest version of develop
* Please adhere to the following branch naming conventions:
  - `feature/my_cool_feature` for feature branches
  - `release/v1.2.3` for release branches
  - `hotfix/missing_dependency` for hot fixes or release maintenance
* Format git commit messages **properly** (see below for more on this)
* Lint the code by running `grunt`
* Add relevant tests to cover the change
* Make sure test-suite passes: `npm test`

## Branching Model

This project follows the git flow branching model. For those unfamiliar, Atlassian provide a [good primer](https://www.atlassian.com/git/tutorials/comparing-workflows/gitflow-workflow) which is where I pinched the below graphic from.

![](http://i.imgur.com/4UZwO5Z.png)

## Git Commit Messages

Firstly, adhering to this isn't a must, but it represents good development practice. A good git commit takes roughly the following form:

* A brief title (prefixed by a tag eg. bug fix, +feature) MAX 50ish chars
* A longer description, written in present tense (eg. "Adds red buttons to home page") limited to 72 chars per line

I've adopted this approach from [this tbaggery post](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html) which many people point to as an early gold standard for commit messages. It points out loads of benefits of following this 'standard'.

[This blog post](http://robots.thoughtbot.com/5-useful-tips-for-a-better-commit-message) which borrows a lot from the tbaggery one offers a neat `.vimrc` addition which helps in sticking to these recommendations.
