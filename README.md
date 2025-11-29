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
  build-docs:
    uses: ./.github/workflows/docc.yml
    with:
      project_target: MyLibrary
      hosting_path: docs
      xcode_version: "16.2"
      macos_version: "macos-15"
```

## License
**github-workflows** is under Apache license. See the [LICENSE](LICENSE) file for more info.
