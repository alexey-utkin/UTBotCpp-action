# Utbot Action

You can use this GitHub Action to create pull requests tests and code analysis info to your repository

## Content

- [Inputs](#inputs)
- [Examples](#examples)

## Inputs

All inputs are 

| Name | Description | Default |
| --- | --- | --- |
| `test_push_info` | Add tests to pull request  | true |
| `test_delete_info` | Delete old tests in pull request | false |

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
```
