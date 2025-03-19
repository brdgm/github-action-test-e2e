github-action-test-e2e
======

Composite GitHub Action to run E2E tests (Playwright) for a brdgm.me application.

Usage example:

```yaml
name: Test E2E

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
