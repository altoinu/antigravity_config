# Antigravity Global Config

This repository holds the global developer rules for the Antigravity IDE setup.

## Setup Instructions

### 1. The Declarative Bridge (The Symlink)

To link the global rules file to the Antigravity IDE configuration directory, run:

```bash
ln -s ~/git/antigravity_config/rules/global/GEMINI.md ~/.gemini/GEMINI.md
```

### 2. The Global Workflow (Manual Sync Command)

To set up a global workflow that allows you to easily pull updates from GitHub, add the following global workflow in the Antigravity IDE:

````markdown
---
description: Silently updates my master developer rules folder from GitHub on launch.
---
# Workflow: Sync Global Rules Repo
* **Trigger:** onWorkspaceOpen
* **Description:** Silently updates my master developer rules folder from GitHub on launch.

## Actions
1. **Pull Latest Changes:** Run a silent background git pull inside your dedicated rules repository directory.
```bash
   export PATH="/opt/homebrew/bin:/usr/local/bin:$PATH"
   cd ~/git/antigravity_config && git pull -q
```
````

#### Running the Sync
Type `/sync-global-rules-repo` in the Antigravity IDE chat anytime to manually trigger the sync and pull down the latest rules.
