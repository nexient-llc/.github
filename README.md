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

### Adding a repo

If a workflow already exists that fits the repos need you can add a topic to the repo and have it included in the sync process.

- In your repo click the gear icon on the right of the of the about section on the right hand side of the code tab.
- In the model under the field label `Topics` type the corrisponding topic relating to the workflow.
- Save your changes, closing the model.
- In the `.github` repo under the actions tab select `sync-global-workflows` in the workflows list.
- Click the `Run workflow` button in the middle right of the page and type the name of your target repository
- Click the green `Run workflow` to execute the workflow

### Resources & Links

- https://github.blog/2017-01-31-introducing-topics/
- https://github.com/derberg/copy-files-to-other-repositories

### Good to Knows & Gotchas

- Should the sync action get triggered upon merge it will only syncronise changes made within the merge. Any prior changes that are not present within the target repos and also not present in the merge will not be synced. If this is the case, manually sync the repo using the stops in `Adding a repo`.