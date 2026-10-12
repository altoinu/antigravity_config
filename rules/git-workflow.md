# Git Workflow Guidelines

## Strict No-Fast-Forward Policy (`--no-ff`)
- Always use `git merge --no-ff` with an explicit, descriptive merge commit message for all branch merges.
- Never perform fast-forward merges so commit topology and branch lifecycles remain clearly visible in GUI Git graph viewers.
