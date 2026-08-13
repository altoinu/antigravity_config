# Antigravity Global Config

This repository holds the global developer rules and workflows for Antigravity IDE.

## Directory Structure

```text
antigravity_config/
├── README.md
├── rules/
│   ├── general.md
│   └── nestjs-database.md
└── global_workflows/
    └── sync-global-rules-repo.md
```

## Setup Instructions

### 1. Link Rules and Workflows

Run the following commands to link this repository to your global Antigravity configuration directory (`~/.gemini/config`):

```bash
mkdir -p ~/.gemini/config
ln -sfn ~/git/antigravity_config/rules ~/.gemini/config/rules
ln -sfn ~/git/antigravity_config/global_workflows ~/.gemini/config/global_workflows
```

> **Note:** Any new `.md` files added to `rules/` or `global_workflows/` will be automatically recognized by Antigravity across all workspaces without requiring any additional symlinks.

### 2. Auto-Sync Workflow

The `/sync-global-rules-repo` workflow is automatically loaded and configured to pull updates on workspace open (`onWorkspaceOpen`).

You can also manually trigger a sync anytime in the Antigravity chat by running:
```text
/sync-global-rules-repo
```
