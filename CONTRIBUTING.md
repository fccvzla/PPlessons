# Contributing to FCC VE Pair Programming

First off, thanks for taking the time to contribute!

The following is a set of guidelines for contributing to FCC VE Pair Programming, which are hosted in the [FCC Venezuela](https://github.com/fccvzla) on GitHub. These are mostly guidelines, not rules. Use your best judgment, and feel free to propose changes to this document in a pull request.

## Table of contents

* [Code of conduct](#code-of-conduct)
* [Motivation](#motivation)
* [Evironment setting and testing](#environment-setting-and-test)
  * [Setting the environment](#Setting-the-environment)
  * [Testing the files](#testing-the-files)
* [How to submit changes](#how-to-submit-changes)
  * [Using the issue templates](#using-the-issue-templates)


## Code of conduct

FCC VE as a learning community is open to all the people who is interested in learning new skills and make friends on the way. We believe in learning as a language and tool to connect with others regardless of age, body size, disability, ethnicity, sex characteristics, gender identity and expression,level of experience, education, socio-economic status, nationality, political orientation, personal appearance, race, religion, or sexual identity and orientation.

We strongly recommend read the [code of conduct file](https://github.com/fccvzla/PPlessons/blob/main/CODE_OF_CONDUCT.md), located on the repository root, If you need a guide and examples of what is the expected behaviour collaborating on this community or if you feel something is not including you in some way or if something is making you feel uncomfortable you will find on that document how to report that to us.

## Motivation

This project brought as idea in our telegram channel to continue with pair programming activities in the community. The main reason of this being a github repository comes out when we thought about the common issues some people in Venezuela face on their daily basis and how we can sort out those problems to keep up delivering knowledge material and guidance.

It is important for us that every contribution take into consideration the following:

1. **This repository must be lightweight as possible.** Some people don’t have a fast internet connection or they haven’t connection at all, in some cases they have to use mobile data to access to the internet. Bear in mind that the average connection speed in Venezuela is close to 3mbps.
  
2. **Any practice contribution should be runned offline or with minimal internet connection.** As been said before internet connection is a real issue in Venezuela post excercises that need uninterrupted internet connection does not help, instead creates a point of frustration for the people that is trying to learn.

3. **Tooling recommendations must be lightweight and low resources consuming.** Aside of internet connection, the technology accesibility is not the best in Venezuela, some people work hard from their phones, (that’s why we have a section of compilers and editor to use in phones), some others have computers with low hardware specs.

4. **Content Sharing must not be copyrighted or banned for Venezuela.** We encourage contributors to share content on this repository preferably open source content via direct link to the content official channels, or paid content with direct link to official stores. Breaking laws or copyright infringement it is not allowed on this community and will be take down immediately.

## Environment setting and test

Given the nature of this repository we do not have unit testing for code. We use markdown files for almost anything. Markdown is lightweight text format that can be formatted, making it perfect for people who don’t have a permanent internet connection, so they can download the files and keep learning.

In order to preserve the good practices, file consistency and readability we use a markdown linter and spell checkers as a way to keep a healthy way to share knowledge, the enforcement of this tools is triggered in a commit hook script.

### Setting the environment

We use [MardownLint-cli](https://github.com/igorshubovych/markdownlint-cli) as linter, [Aspell](http://aspell.net/) as spell checker and [pre-commit](https://pre-commit.com/) to trigger them.

Markdownlint and Aspell is used in many editors plugins, using one on them or similar is also a good practice before test your files, but those tools are necessary to be installed in your system in order to make commits.

Above you have the links to every tools official page were is include the installing/download secrion for your system.

Once you have installed markdownlint, aspell and pre-commit run:

```bash
pre-commit install
```

### Testing the files

File testing is more linting them, because there is nothing to test on mardown files. We tried to automate this task in the commit hook using pre-commit. 

Basically every time you try to commit changes a script will run markdownlint on the files you created/edited. If there are lint errors on the files, you will not be able to commit changes until you fix them.

For now we are figuring out how to automate the spell checkings, so we are recommending to use it before post an issue an resolve the typos

```bash
aspell --markdown-skip-ref-labels --lang=En-us -c myfile.md
```

### Adding words to the aspell dictionary to avoid some spell checkings

Aspell allow us to create a personal dictionary to avoid checking some words, this a powerfull tool but at the same time need to be reviewed constantly to preserve the repository understandably.

## How to submit changes

After you install the required tools to test your submissios you will need to do the following before posting a new pull request:

1. Fork this repository
2. Clone your forked version of this repository
3. [Configure your remote for your fork](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/configuring-a-remote-for-a-fork)
4. Create a new branch in you forked repository and make changes
5. Pull changes from the main repository before push in your forked version
6. [Create a new pull request from your forked repository](https://docs.github.com/en/free-pro-team@latest/github/collaborating-with-issues-and-pull-requests/creating-a-pull-request-from-a-fork)

### Using the issue templates

Issue templates is a tool github offers to make the issues more structured for the reviewers team. We have made some basic templates to post issues and you must use them in order to request a change on this repository as colaborator.

* New Lesson
* New Exercise
* New Example
* Repo Structure suggestion/enhancement
* Documentation
* Bug
