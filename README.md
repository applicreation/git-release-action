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
      - uses: applicreation/versions-action@v2
        id: versions
        with:
          tag: ${{ github.ref_name }}
      - uses: applicreation/git-release-action@v2
        with:
          use_prefix: ${{ steps.versions.outputs.has_prefix }}
          major: ${{ steps.versions.outputs.major }}
          minor: ${{ steps.versions.outputs.minor }}
          patch: ${{ steps.versions.outputs.patch }}
```
