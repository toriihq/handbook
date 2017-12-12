# GitHub

## Why GitHub?

GitHub is the leading git repository hosting service. Most apps have integrations for GitHub, most open source projects can be found on GitHub and it has tools for collaboration.

## Workflow

The flow is targeted for CI/CD where small changes are merged into the master branch and deployed to production.

To keep the flow **simple** and avoid merge conflicts, we use the following steps:

1. Create a new branch from `master`. Any descriptive name will do.
2. Work on your branch and push changes to GitHub.
3. If there are merge conflicts with `master`, resolve the merge locally. Avoid using `rebase` as this adds complexity to all steps.
4. Create a Pull Request to `master`.
5. Once reviewed, `Squash merge` the changes.

Note: `master` should always be deployable, and for most projects – it is automatically deployed.
