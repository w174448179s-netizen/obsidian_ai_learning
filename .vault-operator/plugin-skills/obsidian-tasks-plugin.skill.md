---
id: obsidian-tasks-plugin
name: Tasks
source: vault-native
plugin-type: community
status: enabled
class: FULL
description: "Track tasks across your vault. Supports due dates, recurring tasks, done dates, sub-set of checklist items, and filtering."
has-settings: true
commands:
  - id: "obsidian-tasks-plugin:edit-task"
    name: "Tasks: Create or edit task"
  - id: "obsidian-tasks-plugin:toggle-done"
    name: "Tasks: Toggle task done"
  - id: "obsidian-tasks-plugin:add-query-file-defaults-properties"
    name: "Tasks: Add all Query File Defaults properties"
  - id: "obsidian-tasks-plugin:set-status-symbol-to-space"
    name: "Tasks: Change status to: [ ] Todo"
  - id: "obsidian-tasks-plugin:set-status-symbol-to-x"
    name: "Tasks: Change status to: [x] Done"
  - id: "obsidian-tasks-plugin:set-status-symbol-to-/"
    name: "Tasks: Change status to: [/] In Progress"
  - id: "obsidian-tasks-plugin:set-status-symbol-to--"
    name: "Tasks: Change status to: [-] Cancelled"
---

# Tasks

**Description:** Track tasks across your vault. Supports due dates, recurring tasks, done dates, sub-set of checklist items, and filtering.
**Status:** Enabled
**Plugin ID:** obsidian-tasks-plugin

## Available Commands

Available command IDs (use execute_command for Obsidian-native commands):
- `obsidian-tasks-plugin:edit-task` -- Tasks: Create or edit task
- `obsidian-tasks-plugin:toggle-done` -- Tasks: Toggle task done
- `obsidian-tasks-plugin:add-query-file-defaults-properties` -- Tasks: Add all Query File Defaults properties
- `obsidian-tasks-plugin:set-status-symbol-to-space` -- Tasks: Change status to: [ ] Todo
- `obsidian-tasks-plugin:set-status-symbol-to-x` -- Tasks: Change status to: [x] Done
- `obsidian-tasks-plugin:set-status-symbol-to-/` -- Tasks: Change status to: [/] In Progress
- `obsidian-tasks-plugin:set-status-symbol-to--` -- Tasks: Change status to: [-] Cancelled

## Configuration File

Settings path: `.obsidian/plugins/obsidian-tasks-plugin/data.json`

To configure this plugin programmatically:
1. Read the config: read_file(".obsidian/plugins/obsidian-tasks-plugin/data.json")
2. Understand the settings structure and modify values as needed
3. Write changes: write_file(".obsidian/plugins/obsidian-tasks-plugin/data.json", updatedJSON)

Do NOT ask the user to open Settings UI. Modify data.json directly.

## Current Configuration

These are the plugin's current settings (sensitive values redacted):

```
presets:
  this_file: path includes {{query.file.path}}
  this_folder: folder includes {{query.file.folder}}
  this_folder_only: filter by function task.file.folder === query.file.folder
  this_root: root includes {{query.file.root}}
  hide_date_fields: # Hide any values for all date fields
hide due date
hide scheduled date
hide start date
hide created date
hide done date
hide cancelled date
  hide_non_date_fields: # Hide all the non-date fields, but not tags
hide id
hide depends on
hide recurrence rule
hide on completion
hide priority
  hide_query_elements: # Hide toolbar, postpone, edit and backlinks
hide toolbar
hide postpone button
hide edit button
hide backlinks
  hide_everything: # Hide everything except description and any tags
preset hide_date_fields
preset hide_non_date_fields
preset hide_query_elements
removeGlobalFilter: false
taskFormat: tasksPluginEmoji
setCreatedDate: false
setDoneDate: true
setCancelledDate: true
autoSuggestInEditor: true
autoSuggestMinMatch: 0
autoSuggestMaxItems: 20
useFilenameAsScheduledDate: false
recurrenceOnNextLine: false
removeScheduledDateOnRecurrence: false
searchResults:
  taskCountLocation: bottom
statusSettings:
  coreStatuses: [2 items]
  customStatuses: [2 items]
isShownInEditModal:
  priority: true
  recurrence: true
  due: true
  scheduled: true
  start: true
  before_this: true
  after_this: true
  status: true
  created: true
  done: true
  cancelled: true
dismissedNotices:
  live-preview-callout-warning: false
features:
  INTERNAL_TESTING_ENABLED_BY_DEFAULT: true
headingOpened:
  核心状态: true
  自定义状态: true
debugSettings:
  ignoreSortInstructions: false
  showTaskHiddenData: false
  recordTimings: false
loggingOptions:
  minLevels:
    : info
    tasks: info
    tasks.Cache: info
    tasks.Events: info
    tasks.File: info
    tasks.Query: info
    tasks.Task: info
```
(1 sensitive field(s) redacted)

For full settings, read: `.obsidian/plugins/obsidian-tasks-plugin/data.json`

## Documentation

For detailed plugin documentation (commands, options, dependencies):
read_file(".vault-operator/plugin-skills/obsidian-tasks-plugin.readme.md")

## Usage

When the user asks for functionality related to Tasks:
1. Read the plugin documentation (.readme.md) to understand capabilities and dependencies
2. Read the config file (.obsidian/plugins/obsidian-tasks-plugin/data.json). If it does not exist, that is normal -- create it with the required settings
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
