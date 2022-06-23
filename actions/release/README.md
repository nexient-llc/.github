## Inputs

* `mode`: Sets the versioning type to use. For options see https://github.com/restechnica/semverbot#modes (default: "git-branch")

## Example

```yaml
name: "Run Release"
on: pull_request

jobs:
  release:
    runs-on: nexient-llc/platform-images
    steps:
    - name: checkout source
      uses: actions/checkout@master
    - name: Run Make Release
      uses: nexient-llc/.github/actions/release
      with:
        mode: 'git-branch'
```
