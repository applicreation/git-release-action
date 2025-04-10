# git-release-action

## Usage

```yaml
on:
  release:
    types:
      - published
jobs:
  release:
    runs-on: ubuntu-latest
    steps:  
      - uses: applicreation/git-release-action@v1
```
