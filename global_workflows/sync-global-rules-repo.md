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
git -C ~/git/antigravity_config pull -q
```
