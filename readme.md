# Skitscript Interpreter Test Suite [![License](https://img.shields.io/github/license/skitscript/interpreter-test-suite.svg)](https://github.com/skitscript/interpreter-test-suite/blob/main/license) [![Renovate enabled](https://img.shields.io/badge/renovate-enabled-brightgreen.svg)](https://renovatebot.com/)

A test suite for interpreters of Skitscript documents.

## Installation

It is recommended to install this as a Git submodule and use the included test
cases in your project's test suite:

```bash
git submodule add https://github.com/skitscript/interpreter-test-suite submodules/skitscript/interpreter-test-suite
```

### Renovate Updates

If you are using Renovate in your project, add
[the following](https://docs.renovatebot.com/modules/manager/git-submodules/) to
its `renovate.json` to automatically raise PRs when changes are pushed to this
repository:

```json
{
  "git-submodules": {
    "enabled": true
  }
}
```

## Usage

The [cases](./cases) directory contains a number of subdirectories.  Each
contains a standard set of files:

### [input.skitscript](./cases/four-decisions/input.skitscript)

This is the Skitscript file which is to be fed into the parser, then the
interpreter during the test case.

### [scenarios/*.json](./cases/four-decisions/scenarios/a-a-a-a.json)

These files contain JSON representations of the prompts shown to the user during
a scenario, intercalated with the statement indices selected by the user in
response.

These prompts are similar to
[ValidState](https://github.com/skitscript/interpreter-nodejs/blob/main/ValidState/index.ts).
