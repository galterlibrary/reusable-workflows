# reusable-workflows

This repo hosts Galter's reusable GitHub Action workflows.

## Define

If you think your workflow can be re-used, place it in a separate file in `.github/workflows/`.
Follow the example of other workflows there and/or read up on reusable workflows here:
https://docs.github.com/en/actions/how-tos/sharing-automations/reuse-workflows .

## Use

In one of *your* project's workflows e.g., in the repo `me/my-repo`, the workflow `.github/workflows/my-workflow.yml`,
call the workflow that you want to reuse e.g., `reuse-me.yml`, as follows:

```yml
name: Call a reusable workflow

on:
  pull_request:
    branches:
      - main

jobs:
  call-workflow:
    uses: galterlibrary/reusable-workflows/.github/workflows/reuse-me.yml@main
```

`main` can be replaced by available version if appropriate.
