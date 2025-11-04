---
argument-hint: [--component=<component_name>] [--force] [--dry-run]
description: Updates NioPD from the GitHub repository, optionally specifying a component to update.
---

# Command: /niopd:SYS:update

This command updates the NioPD plugin from the GitHub repository, pulling the latest changes and applying them to your local installation.

## Usage
`/niopd:SYS:update [--component=<component_name>] [--force] [--dry-run]`

## Preflight Checklist

1.  **Check Current Directory:**
    -   Verify that the current directory contains a `niopd` directory with a `commands` subdirectory.
    -   If not, inform the user: "❌ Error: This command must be run from the root of a project that contains the `niopd` directory."

2.  **Check Internet Connectivity:**
    -   Verify internet connectivity to GitHub.
    -   If not connected, inform the user: "❌ Error: No internet connection or GitHub is unreachable."

## Instructions

You are Nio, an AI Product Assistant. Your task is to update the NioPD system from the GitHub repository.

### Step 1: Acknowledge and Prepare
-   Acknowledge the user's request: "On it! I'll update the NioPD system from the GitHub repository."
-   Parse the arguments:
    -   `--component=<component_name>`: If specified, update only the specified component directory.
    -   `--force`: If specified, apply updates even if there are conflicts.
    -   `--dry-run`: If specified, show what would be updated without making changes.

### Step 2: Check Current Installation
-   Determine the current NioPD version by checking the `.claude-plugin/marketplace.json` file if it exists.
-   List the current command directories in `niopd/commands/` to show what components are currently installed.
-   Inform the user of the current version and installed components.

### Step 3: Fetch Updates
-   Inform the user: "Fetching updates from the GitHub repository..."
-   If `--dry-run` is specified, inform the user: "DRY RUN MODE: No changes will be made. This would check for updates and show what would be updated."
-   If `--force` is specified, inform the user: "FORCE MODE: Updates will be applied even if there are conflicts."

### Step 4: Create Backup
-   Create a backup directory with a timestamp: `backup_YYYYMMDD_HHMMSS`
-   Backup critical files:
    -   `.claude-plugin/marketplace.json` (if it exists)
    -   The entire `niopd/commands/` directory
-   Inform the user: "Creating backup in `backup_YYYYMMDD_HHMMSS`"

### Step 5: Apply Updates
-   If `--dry-run` is not specified:
    -   Create a temporary directory for the update.
    -   Clone the repository to the temporary directory.
    -   If `--component` is specified:
        -   Copy only the specified component directory from the repository to the local `niopd/commands/` directory.
        -   Inform the user: "Updating specific component: <component_name>"
    -   If no component is specified:
        -   Copy all command directories from the repository to the local `niopd/commands/` directory.
        -   Inform the user: "Updating full NioPD installation"
    -   Clean up the temporary directory.
-   If `--dry-run` is specified:
    -   Show what would be updated without making changes.
    -   Inform the user: "Would fetch updates from GitHub repository" and what would be updated.

### Step 6: Confirm and Conclude
-   Report the update summary:
    -   Current version
    -   Update target (full or specific component)
    -   Force mode status
    -   Dry run mode status
    -   Backup location
-   Inform the user: "✅ Update completed successfully. Please restart Claude Code to apply the changes."
-   Provide manual update instructions:
    -   "For manual updates, you can also:"
    -   "1. Visit https://github.com/iflow-ai/niopd"
    -   "2. Download the latest release"
    -   "3. Extract to your plugin directory"
    -   "4. Restart Claude Code"
-   Inform the user about the backup: "Note: If you encounter any issues after updating, you can restore from the backup directory: `backup_YYYYMMDD_HHMMSS`"

## Error Handling
-   **Wrong Directory:** If the command is not run from the correct directory, inform the user clearly.
-   **No Internet:** If there's no internet connection, inform the user clearly.
-   **Component Not Found:** If a specified component doesn't exist, inform the user.
-   **Update Failure:** If the update fails, inform the user and suggest manual update or restoring from backup.
