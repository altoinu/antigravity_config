# Antigravity Global Config

This repository holds the global developer rules for the Antigravity IDE setup.

## Setup Instructions

### 1. The Declarative Bridge (The Symlink)

To link the global rules file to the Antigravity IDE configuration directory, run:

```bash
ln -s ~/git/antigravity_config/rules/global/GEMINI.md ~/.gemini/GEMINI.md
```

### 2. The Imperative Engine (The Global Workflow)

To set up automatic pulling of changes whenever a workspace is opened, add the following workflow to your Antigravity IDE settings:

- **Trigger**: `onWorkspaceOpen`
- **Description**: Silently updates the master developer rules folder from GitHub on launch.

#### Actions

1. **Pull Latest Changes**: Run a silent background git pull inside your dedicated rules repository directory.
   ```bash
   cd ~/git/antigravity_config && git pull -q
   ```
