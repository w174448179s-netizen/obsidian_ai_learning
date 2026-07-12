---
id: obsidian-icon-folder
name: Iconize
source: vault-native
plugin-type: community
status: enabled
class: PARTIAL
description: "Add icons to anything you desire in Obsidian, including files, folders, and text."
has-settings: true
commands:
  - id: "obsidian-icon-folder:iconize:set-icon-for-file"
    name: "Iconize: Set icon for file"
---

# Iconize

**Description:** Add icons to anything you desire in Obsidian, including files, folders, and text.
**Status:** Enabled
**Plugin ID:** obsidian-icon-folder

## Available Commands

Available command IDs (use execute_command for Obsidian-native commands):
- `obsidian-icon-folder:iconize:set-icon-for-file` -- Iconize: Set icon for file

## Plugin API

This plugin exposes a JavaScript API. Use call_plugin_api to call these methods:
- `hasOwnProperty` -- call via call_plugin_api("obsidian-icon-folder", "hasOwnProperty", [args])
- `isPrototypeOf` -- call via call_plugin_api("obsidian-icon-folder", "isPrototypeOf", [args])
- `propertyIsEnumerable` -- call via call_plugin_api("obsidian-icon-folder", "propertyIsEnumerable", [args])
- `toString` -- call via call_plugin_api("obsidian-icon-folder", "toString", [args])
- `valueOf` -- call via call_plugin_api("obsidian-icon-folder", "valueOf", [args])
- `toLocaleString` -- call via call_plugin_api("obsidian-icon-folder", "toLocaleString", [args])

Note: Dynamically discovered methods require user approval for each call unless marked as safe in settings.

## Configuration File

Settings path: `.obsidian/plugins/obsidian-icon-folder/data.json`

To configure this plugin programmatically:
1. Read the config: read_file(".obsidian/plugins/obsidian-icon-folder/data.json")
2. Understand the settings structure and modify values as needed
3. Write changes: write_file(".obsidian/plugins/obsidian-icon-folder/data.json", updatedJSON)

Do NOT ask the user to open Settings UI. Modify data.json directly.

## Current Configuration

These are the plugin's current settings (sensitive values redacted):

```
settings:
  migrated: 6
  iconPacksPath: .obsidian/icons
  fontSize: 16
  emojiStyle: native
  recentlyUsedIconsSize: 5
  extraMargin:
    top: 0
    right: 4
    bottom: 0
    left: 0
  iconInTabsEnabled: false
  iconInTitleEnabled: false
  iconInTitlePosition: above
  iconInFrontmatterEnabled: false
  iconInFrontmatterFieldName: icon
  iconColorInFrontmatterFieldName: iconColor
  iconsBackgroundCheckEnabled: false
  iconsInNotesEnabled: true
  iconsInLinksEnabled: true
  iconIdentifier: :
  lucideIconPackType: native
  debugMode: false
  useInternalPlugins: false
```

For full settings, read: `.obsidian/plugins/obsidian-icon-folder/data.json`

## Documentation

For detailed plugin documentation (commands, options, dependencies):
read_file(".vault-operator/plugin-skills/obsidian-icon-folder.readme.md")

## Usage

When the user asks for functionality related to Iconize:
1. Read the plugin documentation (.readme.md) to understand capabilities and dependencies
2. Read the config file (.obsidian/plugins/obsidian-icon-folder/data.json). If it does not exist, that is normal -- create it with the required settings
3. Configure the plugin by writing data.json with the values needed for the task
4. Execute the task using the appropriate tool:
   - For Obsidian-native commands (including file export): use execute_command
   - For CLI-based conversion needing Pandoc/LaTeX: use execute_recipe
   - For data queries: use call_plugin_api
5. If a command opens a UI dialog, tell the user what to click.

CRITICAL RULES:
- Prefer native Obsidian commands over external tools when both can accomplish the task.
- NEVER create fake output files. If the user asks for a PDF/DOCX/image export, use execute_recipe -- do NOT write content to a .pdf file yourself.
- If a dependency is missing (e.g. Pandoc), tell the user what to install.
IMPORTANT: After reading this file, ALWAYS take action or respond. Never end silently.
