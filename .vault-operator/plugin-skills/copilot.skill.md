---
id: copilot
name: Copilot
source: vault-native
plugin-type: community
status: enabled
class: FULL
description: "Your AI Copilot: Chat with Your Second Brain, Learn Faster, Work Smarter."
has-settings: true
commands:
  - id: "copilot:count-word-and-tokens-selection"
    name: "Copilot: Count words and tokens in selection"
  - id: "copilot:count-total-vault-tokens"
    name: "Copilot: Count total tokens in your vault"
  - id: "copilot:chat-toggle-window"
    name: "Copilot: Toggle Copilot Chat Window"
  - id: "copilot:chat-open-window"
    name: "Copilot: Open Copilot Chat Window"
  - id: "copilot:new-chat"
    name: "Copilot: New Copilot Chat"
  - id: "copilot:trigger-quick-command"
    name: "Copilot: Trigger quick command"
  - id: "copilot:clear-local-copilot-index"
    name: "Copilot: Clear local Copilot index"
  - id: "copilot:garbage-collect-copilot-index"
    name: "Copilot: Garbage collect Copilot index (remove files that no longer exist in vault)"
  - id: "copilot:index-vault-to-copilot-index"
    name: "Copilot: Index (refresh) vault"
  - id: "copilot:force-reindex-vault-to-copilot-index"
    name: "Copilot: Force reindex vault"
  - id: "copilot:load-copilot-chat-conversation"
    name: "Copilot: Load Copilot chat conversation"
  - id: "copilot:copilot-list-indexed-files"
    name: "Copilot: List all indexed files (debug)"
  - id: "copilot:copilot-inspect-index-by-note-paths"
    name: "Copilot: Inspect Copilot index by note paths (debug)"
  - id: "copilot:clear-copilot-cache"
    name: "Copilot: Clear Copilot cache"
  - id: "copilot:open-log-file"
    name: "Copilot: Create log file"
  - id: "copilot:clear-log-file"
    name: "Copilot: Clear log file"
  - id: "copilot:add-selection-to-chat-context"
    name: "Copilot: Add selection to chat context"
  - id: "copilot:add-web-selection-to-chat-context"
    name: "Copilot: Add web selection to chat context"
  - id: "copilot:add-custom-command"
    name: "Copilot: Add new custom command"
  - id: "copilot:apply-custom-command"
    name: "Copilot: Apply custom command"
  - id: "copilot:download-youtube-script"
    name: "Copilot: Download YouTube Script (plus)"
  - id: "copilot:trigger-quick-ask"
    name: "Copilot: Quick Ask"
  - id: "copilot:%E6%9E%B6%E6%9E%84%E6%96%87%E6%A1%A3%E5%AE%8C%E6%95%B4%E6%80%A7%E6%A3%80%E6%9F%A5"
    name: "Copilot: 架构文档完整性检查"
  - id: "copilot:%E6%9B%B4%E6%96%B0%E6%80%9D%E7%BB%B4%E5%AF%BC%E5%9B%BE"
    name: "Copilot: 更新思维导图"
  - id: "copilot:%E5%BF%AB%E9%80%9F%E5%AD%A6%E4%B9%A0%E6%80%BB%E7%BB%93"
    name: "Copilot: 快速学习总结"
  - id: "copilot:%E5%BC%95%E5%AF%BC%E4%B8%8B%E4%B8%80%E6%A8%A1%E5%9D%97"
    name: "Copilot: 引导下一模块"
  - id: "copilot:%E5%87%BA%E9%A2%98%E6%B5%8B%E9%AA%8C"
    name: "Copilot: 出题测验"
  - id: "copilot:%E4%BB%A3%E7%A0%81review%E4%B8%8E%E6%94%B9%E8%BF%9B"
    name: "Copilot: 代码review与改进"
  - id: "copilot:translate%20to%20chinese"
    name: "Copilot: Translate to Chinese"
  - id: "copilot:summarize"
    name: "Copilot: Summarize"
  - id: "copilot:simplify"
    name: "Copilot: Simplify"
  - id: "copilot:rewrite%20as%20tweet"
    name: "Copilot: Rewrite as tweet"
  - id: "copilot:rewrite%20as%20tweet%20thread"
    name: "Copilot: Rewrite as tweet thread"
  - id: "copilot:remove%20urls"
    name: "Copilot: Remove URLs"
  - id: "copilot:make%20shorter"
    name: "Copilot: Make shorter"
  - id: "copilot:make%20longer"
    name: "Copilot: Make longer"
  - id: "copilot:generate%20table%20of%20contents"
    name: "Copilot: Generate table of contents"
  - id: "copilot:generate%20glossary"
    name: "Copilot: Generate glossary"
  - id: "copilot:fix%20grammar%20and%20spelling"
    name: "Copilot: Fix grammar and spelling"
  - id: "copilot:explain%20like%20i%20am%205"
    name: "Copilot: Explain like I am 5"
  - id: "copilot:emojify"
    name: "Copilot: Emojify"
  - id: "copilot:clip%20youtube%20transcript"
    name: "Copilot: Clip YouTube Transcript"
  - id: "copilot:clip%20web%20page"
    name: "Copilot: Clip Web Page"
  - id: "copilot:%E6%B2%89%E6%B7%80%E5%88%B0%E6%9E%B6%E6%9E%84%E6%96%87%E6%A1%A3"
    name: "Copilot: 沉淀到架构文档"
  - id: "copilot:%E6%9B%B4%E6%96%B0%E6%AF%8F%E6%97%A5%E5%AD%A6%E4%B9%A0%E8%BF%9B%E5%BA%A6"
    name: "Copilot: 更新每日学习进度"
  - id: "copilot:%E8%AE%B2%E8%A7%A3%E6%A6%82%E5%BF%B5"
    name: "Copilot: 讲解概念"
---

# Copilot

**Description:** Your AI Copilot: Chat with Your Second Brain, Learn Faster, Work Smarter.
**Status:** Enabled
**Plugin ID:** copilot

## Available Commands

Available command IDs (use execute_command for Obsidian-native commands):
- `copilot:count-word-and-tokens-selection` -- Copilot: Count words and tokens in selection
- `copilot:count-total-vault-tokens` -- Copilot: Count total tokens in your vault
- `copilot:chat-toggle-window` -- Copilot: Toggle Copilot Chat Window
- `copilot:chat-open-window` -- Copilot: Open Copilot Chat Window
- `copilot:new-chat` -- Copilot: New Copilot Chat
- `copilot:trigger-quick-command` -- Copilot: Trigger quick command
- `copilot:clear-local-copilot-index` -- Copilot: Clear local Copilot index
- `copilot:garbage-collect-copilot-index` -- Copilot: Garbage collect Copilot index (remove files that no longer exist in vault)
- `copilot:index-vault-to-copilot-index` -- Copilot: Index (refresh) vault
- `copilot:force-reindex-vault-to-copilot-index` -- Copilot: Force reindex vault
- `copilot:load-copilot-chat-conversation` -- Copilot: Load Copilot chat conversation
- `copilot:copilot-list-indexed-files` -- Copilot: List all indexed files (debug)
- `copilot:copilot-inspect-index-by-note-paths` -- Copilot: Inspect Copilot index by note paths (debug)
- `copilot:clear-copilot-cache` -- Copilot: Clear Copilot cache
- `copilot:open-log-file` -- Copilot: Create log file
- `copilot:clear-log-file` -- Copilot: Clear log file
- `copilot:add-selection-to-chat-context` -- Copilot: Add selection to chat context
- `copilot:add-web-selection-to-chat-context` -- Copilot: Add web selection to chat context
- `copilot:add-custom-command` -- Copilot: Add new custom command
- `copilot:apply-custom-command` -- Copilot: Apply custom command
- `copilot:download-youtube-script` -- Copilot: Download YouTube Script (plus)
- `copilot:trigger-quick-ask` -- Copilot: Quick Ask
- `copilot:%E6%9E%B6%E6%9E%84%E6%96%87%E6%A1%A3%E5%AE%8C%E6%95%B4%E6%80%A7%E6%A3%80%E6%9F%A5` -- Copilot: 架构文档完整性检查
- `copilot:%E6%9B%B4%E6%96%B0%E6%80%9D%E7%BB%B4%E5%AF%BC%E5%9B%BE` -- Copilot: 更新思维导图
- `copilot:%E5%BF%AB%E9%80%9F%E5%AD%A6%E4%B9%A0%E6%80%BB%E7%BB%93` -- Copilot: 快速学习总结
- `copilot:%E5%BC%95%E5%AF%BC%E4%B8%8B%E4%B8%80%E6%A8%A1%E5%9D%97` -- Copilot: 引导下一模块
- `copilot:%E5%87%BA%E9%A2%98%E6%B5%8B%E9%AA%8C` -- Copilot: 出题测验
- `copilot:%E4%BB%A3%E7%A0%81review%E4%B8%8E%E6%94%B9%E8%BF%9B` -- Copilot: 代码review与改进
- `copilot:translate%20to%20chinese` -- Copilot: Translate to Chinese
- `copilot:summarize` -- Copilot: Summarize
- `copilot:simplify` -- Copilot: Simplify
- `copilot:rewrite%20as%20tweet` -- Copilot: Rewrite as tweet
- `copilot:rewrite%20as%20tweet%20thread` -- Copilot: Rewrite as tweet thread
- `copilot:remove%20urls` -- Copilot: Remove URLs
- `copilot:make%20shorter` -- Copilot: Make shorter
- `copilot:make%20longer` -- Copilot: Make longer
- `copilot:generate%20table%20of%20contents` -- Copilot: Generate table of contents
- `copilot:generate%20glossary` -- Copilot: Generate glossary
- `copilot:fix%20grammar%20and%20spelling` -- Copilot: Fix grammar and spelling
- `copilot:explain%20like%20i%20am%205` -- Copilot: Explain like I am 5
- `copilot:emojify` -- Copilot: Emojify
- `copilot:clip%20youtube%20transcript` -- Copilot: Clip YouTube Transcript
- `copilot:clip%20web%20page` -- Copilot: Clip Web Page
- `copilot:%E6%B2%89%E6%B7%80%E5%88%B0%E6%9E%B6%E6%9E%84%E6%96%87%E6%A1%A3` -- Copilot: 沉淀到架构文档
- `copilot:%E6%9B%B4%E6%96%B0%E6%AF%8F%E6%97%A5%E5%AD%A6%E4%B9%A0%E8%BF%9B%E5%BA%A6` -- Copilot: 更新每日学习进度
- `copilot:%E8%AE%B2%E8%A7%A3%E6%A6%82%E5%BF%B5` -- Copilot: 讲解概念

## Configuration File

Settings path: `.obsidian/plugins/copilot/data.json`

To configure this plugin programmatically:
1. Read the config: read_file(".obsidian/plugins/copilot/data.json")
2. Understand the settings structure and modify values as needed
3. Write changes: write_file(".obsidian/plugins/copilot/data.json", updatedJSON)

Do NOT ask the user to open Settings UI. Modify data.json directly.

## Current Configuration

These are the plugin's current settings (sensitive values redacted):

```
userId: d4371f0b-f608-41c7-9d4c-b54f331eedee
isPlusUser: false
defaultChainType: llm_chain
defaultModelKey: deepseek-chat|deepseek
embeddingModelKey: openai/text-embedding-3-small|openrouterai
temperature: 0.1
contextTurns: 15
stream: true
defaultSaveFolder: ai学习/📝 每日日志
defaultConversationTag: ai学习草稿
autosaveChat: true
generateAIChatTitleOnSave: true
autoAddActiveContentToContext: true
defaultOpenArea: view
defaultSendShortcut: enter
customPromptsFolder: copilot/copilot-custom-prompts
indexVaultToVectorStore: ON MODE SWITCH
qaExclusions: copilot
enableIndexSync: true
debug: false
maxSourceChunks: 30
enableInlineCitations: true
activeModels: [25 items: {...}, {...}, {...}...]
activeEmbeddingModels: [12 items: {...}, {...}, {...}...]
embeddingRequestsPerMin: 60
embeddingBatchSize: 16
disableIndexOnMobile: true
showSuggestedPrompts: true
showRelevantNotes: true
numPartitions: 1
lexicalSearchRamLimit: 100
promptSortStrategy: timestamp
chatHistorySortStrategy: recent
projectListSortStrategy: recent
projectsFolder: copilot/projects
defaultConversationNoteName: {$topic}@{$date}_{$time}
passMarkdownImages: true
enableAutonomousAgent: true
enableCustomPromptTemplating: true
enableSemanticSearchV3: false
enableSelfHostMode: false
enableMiyo: false
miyoSearchAll: false
selfHostValidationCount: 0
selfHostSearchProvider: firecrawl
enableLexicalBoosts: true
suggestedDefaultCommands: true
autonomousAgentMaxIterations: 4
autonomousAgentEnabledToolIds: [localSearch, readNote, webSearch, pomodoro, youtubeTranscription, writeFile, editFile, updateMemory]
reasoningEffort: low
verbosity: medium
memoryFolderName: copilot/memory
enableRecentConversations: true
maxRecentConversations: 30
enableSavedMemory: true
quickCommandIncludeNoteContext: true
autoIncludeTextSelection: false
autoAddSelectionToContext: true
autoAcceptEdits: true
diffViewMode: split
userSystemPromptsFolder: copilot/system-prompts
defaultSystemPromptTitle: 你是AI应用开发学习导师兼笔记助手。
autoCompactThreshold: 128000
_keychainOnly: true
_keychainVaultId: 146b7e52
```
(22 sensitive field(s) redacted)

For full settings, read: `.obsidian/plugins/copilot/data.json`

## Documentation

For detailed plugin documentation (commands, options, dependencies):
read_file(".vault-operator/plugin-skills/copilot.readme.md")

## Usage

When the user asks for functionality related to Copilot:
1. Read the plugin documentation (.readme.md) to understand capabilities and dependencies
2. Read the config file (.obsidian/plugins/copilot/data.json). If it does not exist, that is normal -- create it with the required settings
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
