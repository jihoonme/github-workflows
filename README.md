# GitHub Actions Workflows

Reusable Action workflow for jihoonme.

## Feature

- ``swift-docc.yml``
    <br>By importing this swift_docc.yml file, you can consolidate duplicates of github_workflows files in a similar family.

```yml
name: Docc

on:
  release:
    types:
      - published
  push:
    branches:
      - main
  workflow_dispatch:

jobs:
  docc:
    name: Docc
    uses: jihoonme/github-workflows/.github/workflows/swift_docc.yml@main
    with:
      project_target: "ProjectTargetName"
      hosting_path: "TargetPath"
      token: "Github Token"
```

## License
**github-workflows** is under Apache license. See the [LICENSE](LICENSE) file for more info.