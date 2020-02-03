0. Introduction
1. Javascript
2. HTML/CSS - Web presentation
3. Frameworks - Jquery/React/Vue/Angular
4. Package Management - NPM/Yarn
5. Debugging - Chrome/Firefox debugger
6. Version Control - Git
7. Testing - Unit/Integration - Jest/Mocha
8. Deployment - CI/CD
9. Documentation - Define your expectations
10. The Product - What to write

# Introduction

The Javascript language has come a long way and the pace of new features only
seems to be increasing. We have a lot of new tooling to help us build,
including some great frameworks.

But even if you know everything about Javascript, what else do you need to know?

# Javascript

JavaScript is the programming language for the web pages, but it also runs other places, like servers.

JavaScript runs when viewing a web page.

JavaScript can read with the contents of the page.

JavaScript can listen for events on the page.

JavaScript can change the contents of the page.

# HTML/CSS

Since JavaScript interacts with the _contents_ of the web page, interactions with the user are performed by manipulating the content of the page.

This means that a solid knowledge of HTML and CSS is crucial to excel when creating complex JavaScript based web applications.

# Frameworks

Manually manipulating the HTML content is one way to update the content of the page, with tooling built to assist with this (such as Jquery) for many years being the industry standard.

In recent years, frameworks have been adapting to keep pace with the complexity of modern JavaScript applications with the implementation of more formal software design patterns, such as structured view and data models.

AngularJS introduced MVC (Model, View, Controller) design pattern, allowing programmers to define data models (the shape of data), template views based on the HTML and controllers to perform actions and update the data and view.

React was designed to simplify updating the web page's HTML by manipulating a _shadow dom_, a copy of what is rendered in HTML so changes can be applied quickly to this copy, from which a changeset can be compiled to reduce the amount of expensive changes which need to bring the HTML content up to date with the new data.
React also introduced the `JSX` syntax, to write XML-like syntax, which React then compiles to JavaScript.

Vue provides an MVVM (Model, View, Viewmodel) architecture, with HTML templating and virtual dom diffing.

# Package Management

Package management a system of tools that automates the process of installing, upgrading, configuring, and removing packages, or pieces of code from a system.

Package management means having the ability to share the work you have build with others.

Package management also means being able to use software written by others to build faster by focussing on solving the unique problems at hand. Who wants to write another router?

The key package manager for JavaScript is `NPM`.

By initializing a project with `npm init`, installing and maintaining dependencies can be handled with relative ease.

E.g. `npm i react`

With an account on `NPM` packages can also be contributed either as public, for sharing with everyone, or private, allowing only access to a group of accounts, such as within an organisation.

# Debugging

The joy of debugging software depends heavily on the tools available.

Most are familiar with `console.log`, but this isn't available in early versions of Internet Explorer. Debugging javascript application used to rely solely on decrypting mystic error messages and a judicious application of `alert("help")`.

There are a number of other debugging tools which can assist, such as the `debugger` keyword, which will pause execution and allow inspection of the application state, similar to setting `breakpoints` in the developer tools. Once execution has been paused, the code can be stepped through one statement at a time to examine the changes in variables at each stage.

# Testing

Testing is how you know something works.

You can manually test something in a browser, and know it works for now, on _your_ computer.
But _writing_ means you know it will continue to work (until the test fails).

Javascript unit testing for small things,

Integration testing, "automated browser testing".

# Version Control

Version Control is crucial in software development.

New features can be built in branches, when development is complete, the
changes in the branch, a Pull Request can be created and reviewed to merge
the changes into the master, or primary branch.

A project would be initalised with `git init`, or an existing repository downloaded with `git clone ...`.

Branches are created as a copy of the current working branch with `git checkout -b newBranchName`

Create some changes, add or remove files and then select the files to add to the git project with `git add .`

Commit your changes to your branch _locally_ with `git commit -m "Changing files"`.

The changes now exist locally in your branch, to push them back to the project (on your branch), you will need to `git push -u origin newBranchName`.

After this, the new branch will be created in GitHub and a _Pull Request_ can be created to request the changes be reviewed and merged into the primary branch.

# Deployment

Deployment is how you get your code into production.

In the past, it might be FTPing a `.zip` file to a server, unzipping the file and moving it into place. Or FTPing the modified files directly.

CI/CD is how you don't worry about pushing to production on Friday at 4pm.

A CI/CD pipeline is integrated with the version control repository and will be launched automatically when new changes are added to the repository.

Your pipeline can be triggered by the pull-requests and build a new version of the program with those changes in a staging environment to run all of the tests and other checks, reporting any failures. If everything passes without issue, the pipeline can also release the updates to the production environment.

# Documentation

Now that you've written the code, it is important to document how it works.

The documentation should primarily cover the expectations and assumptions you've made about the code.

If for no other reason than to help you understand it when it doesn't behave as you expect it to in six months time.

Small comments through a code base can assist when reading and debugging the code, but comprehensive documentation should provide details of the top level interfaces for the application.

# The Product

Agile, waterfall or something in between, you undoubtedly have tickets.
