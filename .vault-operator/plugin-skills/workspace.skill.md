---
id: workspace
name: Workspace
source: core
plugin-type: core
status: enabled
class: FULL
description: "Native workspace operations: PDF export, tab/pane management, file paths"
has-settings: true
commands:
  - id: "workspace:export-pdf"
    name: "Export current note to PDF"
  - id: "workspace:close"
    name: "Close current tab"
  - id: "workspace:split-horizontal"
    name: "Split horizontally"
  - id: "workspace:split-vertical"
    name: "Split vertically"
  - id: "workspace:new-tab"
    name: "New tab"
  - id: "workspace:copy-path"
    name: "Copy file path"
  - id: "workspace:copy-url"
    name: "Copy Obsidian URL"
  - id: "workspace:edit-file-title"
    name: "Rename file"
  - id: "workspace:toggle-pin"
    name: "Toggle pin"
---

Plugin "Workspace" provides core Obsidian workspace operations.

Available commands:
- workspace:export-pdf -- Export the currently open note to PDF using Obsidian's built-in renderer
- workspace:close -- Close the currently active tab
- workspace:split-horizontal -- Split the current pane horizontally
- workspace:split-vertical -- Split the current pane vertically
- workspace:new-tab -- Open a new empty tab
- workspace:copy-path -- Copy the active file's vault-relative path to clipboard
- workspace:copy-url -- Copy an obsidian:// URL for the active file
- workspace:edit-file-title -- Rename the active file inline
- workspace:toggle-pin -- Pin or unpin the active tab (pinned tabs stay open)

workspace:export-pdf is a native Obsidian command -- zero external dependencies, always available.
It renders the note exactly as Obsidian displays it (theme, CSS, plugins applied).
Note: Opens an export dialog. The user must confirm settings and save location.

Use workspace:export-pdf for quick PDF exports. For advanced conversion (custom LaTeX templates, bibliography, DOCX): use execute_recipe with Pandoc instead.

## Configuration File

Settings path: `.obsidian/workspace.json`

To configure this plugin programmatically:
1. Read the config: read_file(".obsidian/workspace.json")
2. Understand the settings structure and modify values as needed
3. Write changes: write_file(".obsidian/workspace.json", updatedJSON)

Do NOT ask the user to open Settings UI. Modify config directly.

## Current Configuration

```
main:
  id: 40ffc02760977f69
  type: split
  children: [1 items: {...}...]
  direction: vertical
left:
  id: a7462fea517c6760
  type: split
  children: [1 items: {...}...]
  direction: horizontal
  width: 300
right:
  id: 284103c11e05ede3
  type: split
  children: [1 items: {...}...]
  direction: horizontal
  width: 565.5
left-ribbon:
  hiddenItems:
    switcher:打开快速切换: false
    graph:查看关系图谱: false
    canvas:新建白板: false
    daily-notes:打开/创建今天的日记: false
    templates:插入模板: false
    command-palette:打开命令面板: false
    bases:新建数据库: false
    obsidian-git:Open Git source control: false
    mermaid-tools:Open Mermaid Toolbar: false
    copilot:Open Copilot Chat: false
    omnisearch:Omnisearch: false
    obsidian-excalidraw-plugin:新建绘图文件: false
    linkmind:打开 linkmind: false
    obsidian-textgenerator-plugin:Generate Text!: false
    obsidian-textgenerator-plugin:Text Generator: Templates Packages Manager: false
active: 0181e571b4317b82
lastOpenFiles: [36 items: ai学习/🏠 Home.md, ai学习/🏗️ 架构/1-接入网关.md, ai学习/📝 每日日志/2026-07-11.md...]
```

For full settings, read: `.obsidian/workspace.json`

## Documentation

For detailed documentation:
read_file(".vault-operator/plugin-skills/workspace.readme.md")

IMPORTANT: After reading this file, ALWAYS take action or respond. Never end silently.
