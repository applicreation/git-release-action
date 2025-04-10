# git-release-action

## Usage

```yaml
on:
  release:
    types:
      - published
permissions:
  contents: write
jobs:
  release:
    runs-on: ubuntu-latest
    steps:  
      - uses: actions/checkout@v4
      - uses: applicreation/git-release-action@v1
```
