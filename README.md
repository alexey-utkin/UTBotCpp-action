# Utbot Action

You can use this GitHub Action to create pull requests tests and code analysis info to your repository

## Content

- [Inputs](#inputs)
- [Installation](#installation)
- [Examples](#examples)

## Inputs

All inputs are required

| Name | Description | required |
| --- | --- | --- | --- |
| `test_push_info` | Add tests to pull request  | Yes |
| `test_delete_info` | Delete old tests in pull request | Yes |
| `utbot_version` | UTBot version to run  | Yes |
| `launch_param` | Valid values are `project`, `directory` and `file` | Yes |
| `param_name` | `directory` or `file` name | 'No' for the 'project', 'Yes' for the rest |

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
      uses: slawa4s/Utbot-Action@test-1.0.1
      with:
        test_push_info: 'true'
        test_delete_info: 'false'
        utbot_version: '1.0.1'
        launch_param: 'project'
```
