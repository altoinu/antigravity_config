# Code Organization & Module File Layout Guidelines

## Top-Down Module Structure
When writing, updating, or refactoring TypeScript/JavaScript module files, code must strictly adhere to the following top-down ordering:
1. **Imports**: External package imports followed by internal workspace imports at the very top.
2. **Interfaces & Types**: Exported and internal type aliases, parameter interfaces, and return contracts.
3. **Constants & Module State**: Module-level constants, configuration defaults, and module state / global variable definitions (caches, maps, trackers).
4. **Private / Internal Helper Functions**: Unexported helper functions and utility logic.
5. **Public / Exported Functions & Classes**: Primary public API routines, lifecycle handlers, and main module exports placed at the bottom.

## Alphabetical Ordering Preference
Whenever practical, order elements within each section alphabetically, as well as:
- Named import and export specifiers
- Object properties and literal keys
- Interface / type definition keys
- Sequential function and constant definitions
- Unit test suites (`describe` blocks) matching the top-down sequence of functions in the source file

### Pragmatic Exceptions
Natural exceptions are always accepted when there is a valid engineering or readability rationale, including:
- **Declaration / Execution Order**: A type, helper, or variable must be defined before its usage or evaluation.
- **Semantic & Domain Grouping**: Grouping closely related data for immediate human readability (e.g. `firstName`, `lastName`; `address1`, `address2`, `city`, `state`, `zip`; `min`, `max`; `x`, `y`).
- **Sequential Workflow Coupling**: Functions that execute in an obvious step-by-step sequence (e.g. `prepareInput()`, `processInput()`, `cleanupInput()`).
- **Framework & Runtime Semantics**: React hook order, Next.js routing exports, or middleware pipelines.
