# Contribution to Windows Musawo

We welcome and appreciate contributions from the community.
There are many ways to become involved with Windows Musawo:
including filing issues,
joining in design conversations,
writing and improving documentation,
and contributing to the code.
Please read the rest of this document to ensure a smooth contribution process.

## Intro to Git and GitHub

* Make sure you have a [GitHub account](https://github.com/signup/free).
* Learning Git:
    * GitHub Help: [Good Resources for Learning Git and GitHub][good-git-resources]
    * [Git Basics](../docs/git/basics.md): install and getting started
* [GitHub Flow Guide](https://guides.github.com/introduction/flow/):
  step-by-step instructions of GitHub Flow


## Reporting Issues

We always welcome bug reports, proposals and overall feedback. Here are a few tips on how you can make reporting your issue as effective as possible.

### Finding Existing Issues

Before filing a new issue, please search our [open issues](https://github.com/OSCA-Kampala-Chapter/Windows-Musawo/issues) to check if it already exists.

If you do find an existing issue, please include your own feedback in the discussion. Do consider upvoting (👍 reaction) the original post, as this helps us prioritize popular issues in our backlog.

### Writing a Good Bug Report

Good bug reports make it easier for maintainers to verify and root cause the underlying problem. The better a bug report, the faster the problem will be resolved. Ideally, a bug report should contain the following information:

* A high-level description of the problem.
* A _minimal reproduction_, i.e. the smallest size of code/configuration required to reproduce the wrong behavior.
* A description of the _expected behavior_, contrasted with the _actual behavior_ observed.
* Information on the environment: OS/distro, CPU arch, SDK version, etc.
* Additional information, e.g. is it a regression from previous versions? are there any known workarounds?

#### Why are Minimal Reproductions Important?

A reproduction lets maintainers verify the presence of a bug, and diagnose the issue using a debugger. A _minimal_ reproduction is the smallest possible console application demonstrating that bug. Minimal reproductions are generally preferable since they:

1. Focus debugging efforts on a simple code snippet,
2. Ensure that the problem is not caused by unrelated dependencies/configuration,
3. Avoid the need to share production codebases.

#### Are Minimal Reproductions Required?

In certain cases, creating a minimal reproduction might not be practical (e.g. due to nondeterministic factors, external dependencies). In such cases you would be asked to provide as much information as possible, for example by sharing a memory dump of the failing application. If maintainers are unable to root cause the problem, they might still close the issue as not actionable. While not required, minimal reproductions are strongly encouraged and will significantly improve the chances of your issue being prioritized and fixed by the maintainers.

#### How to Create a Minimal Reproduction

The best way to create a minimal reproduction is gradually removing code and dependencies from a reproducing app, until the problem no longer occurs. A good minimal reproduction:

* Excludes all unnecessary types, methods, code blocks, source files, nuget dependencies and project configurations.
* Contains documentation or code comments illustrating expected vs actual behavior.
* If possible, avoids performing any unneeded IO or system calls. For example, can the .NET based reproduction be converted to a plain old console app?

## Contributing Changes

Project maintainers will merge changes that improve the product significantly and broadly align with the [Windows Musawo Roadmap](https://github.com/OSCA-Kampala-Chapter/Windows-Musawo/docs/roadmap.md).

Contributions must also satisfy the other published guidelines defined in this document as well as in [pr-guide docs](https://github.com/OSCA-Kampala-Chapter/Windows-Musawo/docs/contributing/pr-guide.md).

### DOs and DON'Ts

Please do:

* **DO** follow our [coding style](https://github.com/OSCA-Kampala-Chapter/Windows-Musawo/docs/coding-style.md) (C# code-specific).
* **DO** give priority to the current style of the project or file you're changing even if it diverges from the general guidelines.
* **DO** include tests when adding new features. When fixing bugs, start with
  adding a test that highlights how the current behavior is broken.
* **DO** keep the discussions focused. When a new or related topic comes up
  it's often better to create new issue than to side track the discussion.
* **DO** clearly state on an issue that you are going to take on implementing it.
* **DO** blog and tweet (or whatever) about your contributions, frequently!

Please do not:

* **DON'T** make PRs for style changes.
* **DON'T** surprise us with big pull requests. Instead, file an issue and start
  a discussion so we can agree on a direction before you invest a large amount
  of time.
* **DON'T** commit code that you didn't write. If you find code that you think is a good fit to add to Windows Musawo, file an issue and start a discussion before proceeding.
* **DON'T** submit PRs that alter licensing related files or headers. If you believe there's a problem with them, file an issue and we'll be happy to discuss it.
* **DON'T** made additions without filing an issue and discussing with us first. See [Review Process](https://github.com/OSCA-Kampala-Chapter/Windows-Musawo/docs/contributing/review-process.md).

### Suggested Workflow

We use and recommend the following workflow:

1. Create an issue for your work.
    - You can skip this step for trivial changes.
    - Reuse an existing issue on the topic, if there is one.
    - Get agreement from the team and the community that your proposed change is a good one.
    - If your change adds a new feature, follow the [Review Process](https://github.com/OSCA-Kampala-Chapter/Windows-Musawo/docs/contributing/review-process.md).
    - Clearly state that you are going to take on implementing it, if that's the case. You can request that the issue be assigned to you. Note: The issue filer and the implementer don't have to be the same person.
2. Create a personal fork of the repository on GitHub (if you don't already have one).
3. In your fork, create a branch off of main (`git checkout -b mybranch`).
    - Name the branch so that it clearly communicates your intentions, such as issue-123 or githubhandle-issue.
    - Branches are useful since they isolate your changes from incoming changes from upstream. They also enable you to create multiple PRs from the same fork.
4. Make and commit your changes to your branch.
    - Please follow our [Commit Messages](#commit-messages) guidance.
5. Add new tests corresponding to your change, if applicable.
6. Build the repository with your changes.
    - Make sure that the builds are clean.
    - Make sure that the tests are all passing, including your new tests.
7. Create a pull request (PR) against the Windows-Musawo repository's **main** branch.
    - State in the description what issue or improvement your change is addressing.
8. Wait for feedback or approval of your changes from the maintainers.
    - Details about the pull request [review procedure](https://github.com/OSCA-Kampala-Chapter/Windows-Musawo/docs/contributing/pr-guide.md).
9. When maintainers have signed off, and all checks are green, your PR will be merged.
    - The next official build will automatically include your change.
    - You can delete the branch you used for making the change.

### Help Wanted (Up for Grabs)

The team marks the most straightforward issues as [good first issue](https://github.com/OSCA-Kampala-Chapter/Windows-Musawo/issues?q=is%3Aissue+is%3Aopen+label%3A%22good+first+issue%22). This set of issues is the place to start if you are interested in contributing but new to the codebase.

### Commit Messages

Please format commit messages as follows (based on [A Note About Git Commit Messages](http://tbaggery.com/2008/04/19/a-note-about-git-commit-messages.html):

```
Summarize change in 50 characters or less

Provide more detail after the first line. Leave one blank line below the
summary and wrap all lines at 72 characters or less.

If the change fixes an issue, leave another blank line after the final
paragraph and indicate which issue is fixed in the specific format
below.

Fix #42
```

Also do your best to factor commits appropriately, not too large with unrelated things in the same commit, and not too small with the same small change applied N times in N different commits.

### File Headers

The following file header is the used for files in this repo. Please use it for new files.

```
// Licensed to the OSCA Kampala under one or more agreements.
// The OSCA Kampala licenses this file to you under the MIT license.
```

### PR - CI Process

The Windows Musawo continuous integration (CI) system will automatically perform the required builds and run tests (including the ones you are expected to run) for PRs. Builds and test runs must be clean.

If the CI build fails for any reason, the PR issue will be updated with a link that can be used to determine the cause of the failure.

### PR Feedback

OSCA Kampala team and community members will provide feedback on your change. Community feedback is highly valued. You will often see the absence of team feedback if the community has already provided good review feedback.

One or more OSCA Kampala team members will review every PR prior to merge. They will often reply with "LGTM, modulo comments". That means that the PR will be merged once the feedback is resolved. "LGTM" == "looks good to me".

There are lots of thoughts and [approaches](https://github.com/OSCA-Kampala-Chapter/Windows-Musawo/docs/contributing/emoji.md#emoji) for how to efficiently discuss changes. It is best to be clear and explicit with your feedback. Please be patient with people who might not understand the finer details about your approach to feedback.