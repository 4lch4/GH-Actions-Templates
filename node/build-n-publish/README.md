# Build & Publish

This directory contains 3 GitHub Action workflows that can be used to build and publish a Node.js package to either [NPM][0], [GitHub Packages][1], or [both][2].

## Workflow(s) Breakdown

### Node.js

Each of the Node.js templates are designed with the following conditions/notes in mind:

- Triggers
  - When a new tag that starts with `v` is created.
  - When a new release is created.
  - When manually run from the Actions tab.
- Steps (each step is required to pass before the next step is run)
  - Checkout the repository.
  - Setup Node.js for versions 18 & 20.
  - Install dependencies.
  - Build the package.
  - Test the package.
  - Publish the package.

[0]: ./build-n-publish.yml
[1]: ./build-n-publish-gh.yml
[2]: ./build-n-publish-gh-npm.yml
