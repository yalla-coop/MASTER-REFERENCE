# Code Review Processes
>**what is a code review, really?** Code review is a time to discuss and debate code that is going to be owned by the team going forward. A member, or members of the team will write the code, and the rest of the team, or a subset will determine if it’s at a standard such that’ll be a good value add to the codebase.


## Commit style

### Commit related to one change

- Each commit must be related to a specific change
- Relate the commit to issue, add `Relates/Resolves/Fixes #<issue number>` in the commit body, so the reviewer can track commits logs and know what each commit does/solve.

### Small commits
Keep your commit small as possible, e.g fixing two bugs should be in two commits. keeps your commits small and, again, helps you commit only related changes. 

### complete commit

- commit your changes when they are completed logically.
- don't commit half-done work
- split the feature's logic into chunks that can be completed separately.

### commit with no failed tests

- run the test before each commit.
- don't make commit when a test fails, the goal of committing is to add reference points you sure that the code works fine at, so when a bug appears you can go back to the commits that work fine.


### Make sure there is no eslint errors/warnings:

- You should fix all eslint errors/warnings as you going (_dont wait til the end_), check for eslint warnings on each file before `commit` it.
- every single commit could be linted — everyone should be responsible for committing work without errors.
- Before submitting a PR run `npm run eslint` which must be listed in the `package.json` scripts as `"eslint": eslint .`, running this script will run eslint through all files, and the result will be a list of errors/warnings and their path/file.

### descriptive/detailed commit message

- use good description for the commit message, that describes the major changes that the commit comes with.
- recommendation: see the commit Udacity commit structure [Udacity Git Commit Message Style Guide
](https://udacity.github.io/git-styleguide/)


## Before submitting your Pull Request:

For the PR submitter, here is some point to check before rising a PR to get a good review on your PR:

### Test it locally

Before opening new PR make sure that your PR is passing all tests locally.

### share new `env` variables

- If your PR require new env variables then share them with the team on the project chat channel.
- add or ask the DevOps to add them into `Heroku` and `Travis`

### Add documentation comments
>“Good code is self-documenting.”

- Add comments to your code make it super **Readable**

## Opening new PR
- copy this template and paste it in the PR description
- make sure you went through all the points in the checklist
- take a gif recording for the UI (recommendation: use [Peek](https://github.com/phw/peek))
- request the team review
- if you think that this PR may affect another feature and you need the reviewer to test it carefully then mention it in the description.
- if you need a specific review from one of the team then mention him


# for reviewer 

>**reviewing code is work.**

So, take your time with code reviews. It’s okay to spend many hours reviewing code.
Be sure to click through the commits and PR description for more context before you start reading code. If the reviewer has questions, tend to those as well, and take your time.

if there is any question ask the submitter to clarify it in comments. if there is anything you feel that the team must know about mention them.

go through the checklist points. and make sure all of them are done.
