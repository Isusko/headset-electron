# Contributing to Headset

Welcome to the Headset community!

## Community

We have two main channels of communication:
- our Slack workspace: https://tinyurl.com/y7m8y5x4
- issues on GitHub

If you have any questions on where to start and/or how to proceed, let us know!

## Ways to contribute

We welcome many ways of contributing to Headset:
- finding bugs and [reporting issues](https://github.com/headsetapp/headset-electron/issues)
- picking and working on an existing [issue](https://github.com/headsetapp/headset-electron/labels/help-wanted) marked as 
  "help wanted"
- proposing and implementing improvements to Headset

## Setting up the environment

1. Fork the repository on GitHub

2. Clone your fork of the repository

  ```shell
  git clone https://github.com/<your-username>/headset-electron.git
  ```

3. Install all required dependencies:

    ```shell
    npm ci
    ```

4. Now you can run the app:

  ```shell
  npm run headset
  ```

You are ready to pick a "help wanted" issue and start working on it.

## Testing

Whenever you work on a new feature, be sure to add appropriate tests if necessary.
When testing the app itself, make sure you package for the OS your testing by first running:

```shell
npm run pack:<os>
```
where `<os>` is either `darwin`, `linux` or `windows`.

Before submitting your changes, you should run all the test suites to make sure it works as expected.

1. Linter tests

    ```shell
    npm run lint
    ```

2. General test suites

    ```shell
    npm run test:app
    ```
    Remember that the tests are OS-specific.
    You need to run them on the system you're testing for, using either physical or virtual machines.

## Merging your changes

We work in a pull request driven flow. If you don't know how to make a PR,
[here](https://help.github.com/articles/creating-a-pull-request/) is a GitHub doc on it.

It's best to talk about code and share it early, so you can make a pull request 
even if you haven't finished, or it has errors - it's much easier to improve once other contributors can
see the code! Just make sure to write it in the pull request message and ask for help.

To submit a pull request:
- create a feature branch locally and commit all your changes to it
- run all the relevant tests (linter and general), fix any issues
- push them to a feature branch on your fork - if you do `git push origin <branch-name>`.
  GitHub will automatically create a new branch for you
- go to your GitHub fork, switch to the feature branch and submit a pull request to
  the main repository

Make sure to add relevant information, e.g.:
- which issue you are working on - you can link it using `#<issue-number>` in your message
- which parts of the feature you'd like some feedback on
- where you got stuck if you need help
