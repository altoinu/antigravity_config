# Code Modification & Pair Programming Safety Guidelines

## Explicit User Authorization & No Unsolicited Changes
- **No Unsolicited or Silent Code Changes**: The AI agent must NEVER proactively modify, refactor, or commit source code behind the user's back during informational queries, discussions, or code inspections.
- **Explicit User Initiation Required**: All code modifications, bug fixes, and refactors MUST be explicitly initiated only after presenting findings/discrepancies to the user and receiving the user's direct instruction or approval to proceed.
- **Scope Discipline**: Only change the section of the code explicitly related to what is being discussed. Do not make unnecessary changes to unrelated sections.
- **Preserve Existing Implementations**: Do not simply remove or heavily modify existing parts of the code unless specifically asked or strictly required for the update. Explain the reasoning clearly before modifying or removing existing code.
- **No Assumptions on Data Types**: Do not make assumptions about data types (e.g., changing a variable from a string to a number just because its column name contains "id"). Explain the reasoning first if an update is needed.
- **Complete Representation**: If the internal file representation seems incomplete or optimized, notify the user and ask for the full version before proceeding with modifications.

## Rule & Customization Modification Guidelines
- **User Review Required**: Before creating, modifying, or committing any files, rules, skills, or instructions within customization directories (e.g. `.agents/`, `~/.gemini/config/`, or `antigravity_config/`), the AI agent MUST explicitly present the proposed changes to the user and obtain their confirmation before proceeding.
