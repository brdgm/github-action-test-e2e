github-action-test-e2e
======

Composite GitHub Action to run Playwright tests for a brdgm.me application.

Usage example:

```yaml
name: Test Playwright

on:
  push:
    branches-ignore:
      - experimental/**
      - master
  pull_request:
    branches-ignore:
      - experimental/**
      - master
  workflow_dispatch:

jobs:
  build:
    runs-on: ubuntu-latest
    container:
      image: mcr.microsoft.com/playwright:v1.51.1-noble
      options: --user 1001

    steps:
      - uses: brdgm/github-action-test-e2e@v1
```
