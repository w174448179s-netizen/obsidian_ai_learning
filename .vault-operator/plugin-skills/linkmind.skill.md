---
id: linkmind
name: linkmind
source: vault-native
plugin-type: community
status: enabled
class: FULL
description: "Edit Markdown as a clean, keyboard-friendly mind map."
has-settings: true
commands:
  - id: "linkmind:create-linkmind-note"
    name: "linkmind: 新建思维导图"
  - id: "linkmind:open-linkmind-view"
    name: "linkmind: 以思维导图打开当前笔记"
  - id: "linkmind:return-to-markdown"
    name: "linkmind: 返回 Markdown 编辑器"
  - id: "linkmind:add-child-node"
    name: "linkmind: 添加子节点"
  - id: "linkmind:add-sibling-node"
    name: "linkmind: 添加同级节点"
  - id: "linkmind:duplicate-node"
    name: "linkmind: 复制选中节点"
  - id: "linkmind:move-node-up"
    name: "linkmind: 上移选中节点"
  - id: "linkmind:move-node-down"
    name: "linkmind: 下移选中节点"
  - id: "linkmind:indent-node"
    name: "linkmind: 缩进选中节点"
  - id: "linkmind:outdent-node"
    name: "linkmind: 取消缩进选中节点"
  - id: "linkmind:edit-selected-node"
    name: "linkmind: 编辑选中节点"
  - id: "linkmind:delete-selected-node"
    name: "linkmind: 删除选中节点"
  - id: "linkmind:toggle-selected-node"
    name: "linkmind: 折叠/展开选中节点"
  - id: "linkmind:set-node-emoji"
    name: "linkmind: 设置选中节点 Emoji"
  - id: "linkmind:clear-node-emoji"
    name: "linkmind: 清除选中节点 Emoji"
  - id: "linkmind:add-node-tag"
    name: "linkmind: 给选中节点添加标签"
  - id: "linkmind:clear-node-tags"
    name: "linkmind: 清除选中节点标签"
  - id: "linkmind:select-all-nodes"
    name: "linkmind: 选择全部节点"
  - id: "linkmind:expand-all-nodes"
    name: "linkmind: 展开全部节点"
  - id: "linkmind:collapse-all-nodes"
    name: "linkmind: 折叠全部节点"
  - id: "linkmind:fit-mind-map"
    name: "linkmind: 适应窗口"
  - id: "linkmind:focus-selected-node"
    name: "linkmind: 聚焦选中节点"
  - id: "linkmind:search-nodes"
    name: "linkmind: 搜索节点"
  - id: "linkmind:filter-by-tag"
    name: "linkmind: 按标签过滤"
  - id: "linkmind:clear-tag-filter"
    name: "linkmind: 清除标签过滤"
  - id: "linkmind:toggle-outline"
    name: "linkmind: 显示/隐藏大纲"
  - id: "linkmind:copy-node-link"
    name: "linkmind: 复制选中节点链接"
  - id: "linkmind:copy-branch-markdown"
    name: "linkmind: 复制选中分支为 Markdown"
  - id: "linkmind:paste-markdown-child"
    name: "linkmind: 粘贴 Markdown 为子节点"
  - id: "linkmind:paste-markdown-sibling"
    name: "linkmind: 粘贴 Markdown 为同级节点"
  - id: "linkmind:export-svg"
    name: "linkmind: 导出思维导图为 SVG"
  - id: "linkmind:export-png"
    name: "linkmind: 导出思维导图为 PNG"
  - id: "linkmind:export-selected-svg"
    name: "linkmind: 导出选中分支为 SVG"
  - id: "linkmind:export-selected-png"
    name: "linkmind: 导出选中分支为 PNG"
---

# linkmind

**Description:** Edit Markdown as a clean, keyboard-friendly mind map.
**Status:** Enabled
**Plugin ID:** linkmind

## Available Commands

Available command IDs (use execute_command for Obsidian-native commands):
- `linkmind:create-linkmind-note` -- linkmind: 新建思维导图
- `linkmind:open-linkmind-view` -- linkmind: 以思维导图打开当前笔记
- `linkmind:return-to-markdown` -- linkmind: 返回 Markdown 编辑器
- `linkmind:add-child-node` -- linkmind: 添加子节点
- `linkmind:add-sibling-node` -- linkmind: 添加同级节点
- `linkmind:duplicate-node` -- linkmind: 复制选中节点
- `linkmind:move-node-up` -- linkmind: 上移选中节点
- `linkmind:move-node-down` -- linkmind: 下移选中节点
- `linkmind:indent-node` -- linkmind: 缩进选中节点
- `linkmind:outdent-node` -- linkmind: 取消缩进选中节点
- `linkmind:edit-selected-node` -- linkmind: 编辑选中节点
- `linkmind:delete-selected-node` -- linkmind: 删除选中节点
- `linkmind:toggle-selected-node` -- linkmind: 折叠/展开选中节点
- `linkmind:set-node-emoji` -- linkmind: 设置选中节点 Emoji
- `linkmind:clear-node-emoji` -- linkmind: 清除选中节点 Emoji
- `linkmind:add-node-tag` -- linkmind: 给选中节点添加标签
- `linkmind:clear-node-tags` -- linkmind: 清除选中节点标签
- `linkmind:select-all-nodes` -- linkmind: 选择全部节点
- `linkmind:expand-all-nodes` -- linkmind: 展开全部节点
- `linkmind:collapse-all-nodes` -- linkmind: 折叠全部节点
- `linkmind:fit-mind-map` -- linkmind: 适应窗口
- `linkmind:focus-selected-node` -- linkmind: 聚焦选中节点
- `linkmind:search-nodes` -- linkmind: 搜索节点
- `linkmind:filter-by-tag` -- linkmind: 按标签过滤
- `linkmind:clear-tag-filter` -- linkmind: 清除标签过滤
- `linkmind:toggle-outline` -- linkmind: 显示/隐藏大纲
- `linkmind:copy-node-link` -- linkmind: 复制选中节点链接
- `linkmind:copy-branch-markdown` -- linkmind: 复制选中分支为 Markdown
- `linkmind:paste-markdown-child` -- linkmind: 粘贴 Markdown 为子节点
- `linkmind:paste-markdown-sibling` -- linkmind: 粘贴 Markdown 为同级节点
- `linkmind:export-svg` -- linkmind: 导出思维导图为 SVG
- `linkmind:export-png` -- linkmind: 导出思维导图为 PNG
- `linkmind:export-selected-svg` -- linkmind: 导出选中分支为 SVG
- `linkmind:export-selected-png` -- linkmind: 导出选中分支为 PNG

## Configuration File

Settings path: `.obsidian/plugins/linkmind/data.json`

To configure this plugin programmatically:
1. Read the config: read_file(".obsidian/plugins/linkmind/data.json")
2. Understand the settings structure and modify values as needed
3. Write changes: write_file(".obsidian/plugins/linkmind/data.json", updatedJSON)

Do NOT ask the user to open Settings UI. Modify data.json directly.

## Current Configuration

These are the plugin's current settings (sensitive values redacted):

```
autoSaveDelay: 300
branchColors: [#5b8def, #45b36b, #e89b3c, #9b72e7, #df6f9f]
defaultExpandDepth: 99
animations: true
layoutDirection: right
exportScale: 2
exportTransparentBackground: false
language: zh
showAssociationLinks: true
hideNodeBorders: false
nodeBorderRadius: 10
nodeBorderWidth: 3
nodeBgColor: transparent
mindMapFiles: [ai学习/🧠 思维导图/AI应用开发学习.md]
```

For full settings, read: `.obsidian/plugins/linkmind/data.json`

## Documentation

For detailed plugin documentation (commands, options, dependencies):
read_file(".vault-operator/plugin-skills/linkmind.readme.md")

## Usage

When the user asks for functionality related to linkmind:
1. Read the plugin documentation (.readme.md) to understand capabilities and dependencies
2. Read the config file (.obsidian/plugins/linkmind/data.json). If it does not exist, that is normal -- create it with the required settings
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
