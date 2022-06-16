# GitHub Meta Repository

- [Workflows](#workflows)
    - [Topic Naming Convention](#topic-naming-convention)
    - [Adding a Workflow](#adding-a-workflow)
    - [Resources & Links](#resources--links)

## Workflows

### Topic Naming Convention

Topics are GitHub's eqivilent of tags, and are used by our pipeline for distributing GHA workflows to their respective repositories.

The repo prefix is itself prefixed witht the higher level team managing the repo.

`<team>-<repo-prefix>`

**Examples:**
- platform-tf-module
- platform-module-manifest
- platform-component
- platform-images
- platform-magicdust

### Adding a Workflow

- Update `.github/workflows/sync-global-workflows.yml` to sync with associated topics
- Create/Commit workflow file to the .github/workflows directory
- Manually disable new workflow in this repo if it does not apply to the .github repo

### Resources & Links

- https://github.blog/2017-01-31-introducing-topics/
- https://github.com/derberg/copy-files-to-other-repositories
