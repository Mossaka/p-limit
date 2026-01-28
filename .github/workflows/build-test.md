---
name: Build and Test
on:
  push:
    branches: [main]
  pull_request:
    branches: [main]
  workflow_dispatch:

engine:
  id: copilot
  model: claude-sonnet-4

network:
  firewall: true
  allowed:
    - defaults
    - github
    - "*.npmjs.org"
    - "registry.npmjs.org"

tools:
  bash:
    - "*"
---

# Build and Test p-limit

You are a CI/CD agent. Your job is to build and test this Node.js project.

## Steps

1. Install dependencies:
   ```
   npm install
   ```

2. Run the test suite:
   ```
   npm test
   ```

3. Report the results - if tests pass, indicate success. If they fail, analyze the error output and report what went wrong.
