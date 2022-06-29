# Utbot Action

You can use this GitHub Action to create pull requests tests and code analysis info to your repository

## Content

- [Inputs](#inputs)
- [Installation](#installation)
- [Examples](#examples)

## Inputs

All inputs are required
add_tests, refresh_tests, tests_scope, scope_path
| Name | Type | Description | Required |
| --- | --- | --- | --- |
| `add_tests` | 'true' / 'false' | Add tests to pull request  | `Yes` |
| `refresh_tests` | 'true' / 'false' | Delete old tests in pull request | `Yes` |
| `utbot_version` | xxxx.xx[.xx] | UTBot version to run  | `Yes` |
| `scope` |  `project` / `directory` / `file` | Testing scope | `Yes` |
| `path` | Realtive path string | `directory` or `file` path | `No` for the `project`, `Yes` for the rest |

## Installation

* ```Settings > Actions > Allow GitHub Actions to create and approve pull requests```
* ```permissions: write-all``` line at action before using Utbot Action

## Examples

```yml
on:
  workflow_dispatch:
    
jobs:
  build:
    runs-on: ubuntu-latest
    permissions: write-all
    steps:
    - name: UTBot code analysis
      uses: slawa4s/Utbot-Action@test-1.0.26
      with:
        add_tests: 'true'
        refresh_tests: 'false'
        utbot_version: '2022.06.13'
        scope: 'project'
```
