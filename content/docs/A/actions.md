---
title: "Actions by GitHub"
weight: 4
description: >
  Automate your development process with GitHub Actions
---

To quickly see GitHub Actions in _action_, check out the `.github` directory in the source code of this website [here](https://github.com/DSC-VJTI/a-z-cloud/tree/main/.github). You can see the following directory structure:

```
.github
├── dependabot.yml
└── workflows
    └── gh-pages.yaml
```

There is a `.yaml` or YAML (which stands for YAML Ain't Markup Language) file that defines some workflow or a set of tasks that will be run on each _event_ on the GitHub repository.

### What is an _event_?

An event is a specific change made to your GitHub repository that should trigger your desired workflow. This event can be a new push, a new issue or a pull request made to the repository.

### What is a _workflow_?

A set of automated tasks that are to be run of a specific event. A workflow is composed of several _jobs_ and is defined in a YAML file such as specified above with `gh-pages.yaml`. This is how this file looks:

```yaml
name: GitHub Pages

on:
  push:
    branches:
      - main # Set a branch to deploy
  pull_request:

jobs:
  deploy:
    runs-on: ubuntu-20.04
    concurrency:
      group: ${{ github.workflow }}-${{ github.ref }}
    steps:
      - uses: actions/checkout@v3
        with:
          submodules: true # Fetch Hugo themes (true OR recursive)
          fetch-depth: 1 # Fetch all history for .GitInfo and .Lastmod

      - name: Setup Hugo
        uses: peaceiris/actions-hugo@v2
        with:
          hugo-version: "latest"
          extended: true

      - name: Build
        run: git submodule update --init --recursive --depth 1 && npm i && hugo

      - name: Deploy
        uses: peaceiris/actions-gh-pages@v3
        if: ${{ github.ref == 'refs/heads/main' }}
        with:
          github_token: ${{ secrets.GITHUB_TOKEN }}
          publish_dir: ./public
```

There are 2 keywords to focus on in this file - **on** and **jobs**. **on** is where you define the event/s that should trigger this workflow and **jobs** are the set of tasks that should execute as a part of the workflow.

### Learn

GitHub Actions is a powerful tool to have in your development arsenal. Learn more from the official [documentation](https://docs.github.com/en/actions).
