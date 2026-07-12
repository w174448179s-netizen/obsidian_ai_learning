---
id: obsidian-excalidraw-plugin
name: Excalidraw
source: vault-native
plugin-type: community
status: enabled
class: FULL
description: "Sketch Your Mind. Edit and view Excalidraw drawings. Enter the world of 4D Visual PKM."
has-settings: true
commands:
  - id: "obsidian-excalidraw-plugin:excalidraw-convert-image-from-url-to-local-file"
    name: "Excalidraw: 从 URL 下载图片到本地"
  - id: "obsidian-excalidraw-plugin:excalidraw-unzip-file"
    name: "Excalidraw: 解压当前 Excalidraw 文件"
  - id: "obsidian-excalidraw-plugin:excalidraw-publish-svg-check"
    name: "Excalidraw: Obsidian Publish：搜索过期的 SVG 和 PNG 导出文件"
  - id: "obsidian-excalidraw-plugin:excalidraw-embeddable-poroperties"
    name: "Excalidraw: Embeddable 元素设置"
  - id: "obsidian-excalidraw-plugin:excalidraw-embeddables-relative-scale"
    name: "Excalidraw: 使元素的缩放级别等于当前绘图的缩放级别"
  - id: "obsidian-excalidraw-plugin:open-image-excalidraw-source"
    name: "Excalidraw: 打开 Excalidraw 绘图"
  - id: "obsidian-excalidraw-plugin:excalidraw-disable-autosave"
    name: "Excalidraw: 临时禁用自动保存功能，直到本次 Obsidian 退出（小白慎用！）"
  - id: "obsidian-excalidraw-plugin:excalidraw-enable-autosave"
    name: "Excalidraw: 启用自动保存功能"
  - id: "obsidian-excalidraw-plugin:excalidraw-toggle-session-view-mode"
    name: "Excalidraw: 切换所有 Excalidraw 绘图的查看模式，直到本次 Obsidian 退出"
  - id: "obsidian-excalidraw-plugin:excalidraw-download-lib"
    name: "Excalidraw: 导出 stencil 库为 *.excalidrawlib 文件"
  - id: "obsidian-excalidraw-plugin:excalidraw-open-sidepanel"
    name: "Excalidraw: 打开 Excalidraw 侧边面板"
  - id: "obsidian-excalidraw-plugin:excalidraw-open"
    name: "Excalidraw: 打开已有的绘图 - 于新面板"
  - id: "obsidian-excalidraw-plugin:excalidraw-open-on-current"
    name: "Excalidraw: 打开已有的绘图 - 于当前面板"
  - id: "obsidian-excalidraw-plugin:excalidraw-insert-transclusion"
    name: "Excalidraw: 嵌入绘图 ![[drawing]] 到当前 Markdown 文档中"
  - id: "obsidian-excalidraw-plugin:excalidraw-insert-last-active-transclusion"
    name: "Excalidraw: 嵌入最近编辑过的绘图 ![[drawing]] 到当前 Markdown 文档中"
  - id: "obsidian-excalidraw-plugin:excalidraw-autocreate"
    name: "Excalidraw: 新建绘图 - 于新面板"
  - id: "obsidian-excalidraw-plugin:excalidraw-autocreate-newtab"
    name: "Excalidraw: 新建绘图 - 于新标签页"
  - id: "obsidian-excalidraw-plugin:excalidraw-autocreate-on-current"
    name: "Excalidraw: 新建绘图 - 于当前面板"
  - id: "obsidian-excalidraw-plugin:excalidraw-autocreate-popout"
    name: "Excalidraw: 新建绘图 - 于新窗口"
  - id: "obsidian-excalidraw-plugin:excalidraw-autocreate-and-embed"
    name: "Excalidraw: 新建绘图 - 于新面板 - 并嵌入到当前 Markdown 文档中"
  - id: "obsidian-excalidraw-plugin:excalidraw-autocreate-and-embed-new-tab"
    name: "Excalidraw: 新建绘图 - 于新标签页 - 并嵌入到当前 Markdown 文档中"
  - id: "obsidian-excalidraw-plugin:excalidraw-autocreate-and-embed-on-current"
    name: "Excalidraw: 新建绘图 - 于当前面板 - 并嵌入到当前 Markdown 文档中"
  - id: "obsidian-excalidraw-plugin:excalidraw-autocreate-and-embed-popout"
    name: "Excalidraw: 新建绘图 - 于新窗口 - 并嵌入到当前 Markdown 文档中"
  - id: "obsidian-excalidraw-plugin:run-ocr"
    name: "Excalidraw: OCR 整个绘图：识别涂鸦和图片里的文本并复制到剪贴板和笔记属性中"
  - id: "obsidian-excalidraw-plugin:rerun-ocr"
    name: "Excalidraw: 重新 OCR 整个绘图：识别涂鸦和图片里的文本并复制到剪贴板和笔记属性中"
  - id: "obsidian-excalidraw-plugin:run-ocr-selectedelements"
    name: "Excalidraw: OCR 选中的元素：识别涂鸦和图片里的文本并复制到剪贴板"
  - id: "obsidian-excalidraw-plugin:search-text"
    name: "Excalidraw: 搜索文本"
  - id: "obsidian-excalidraw-plugin:fullscreen"
    name: "Excalidraw: 切换全屏模式"
  - id: "obsidian-excalidraw-plugin:disable-binding"
    name: "Excalidraw: 开启或关闭绑定"
  - id: "obsidian-excalidraw-plugin:disable-framerendering"
    name: "Excalidraw: 开启或关闭画框渲染"
  - id: "obsidian-excalidraw-plugin:frame-settings"
    name: "Excalidraw: 画框设置"
  - id: "obsidian-excalidraw-plugin:copy-link-to-drawing"
    name: "Excalidraw: 复制绘图的 ![[drawing]] 链接"
  - id: "obsidian-excalidraw-plugin:disable-frameclipping"
    name: "Excalidraw: 开启或关闭画框裁切"
  - id: "obsidian-excalidraw-plugin:export-image"
    name: "Excalidraw: 导出为图片"
  - id: "obsidian-excalidraw-plugin:save"
    name: "Excalidraw: 保存（同时更新嵌入了该绘图的 Markdown 文档）"
  - id: "obsidian-excalidraw-plugin:toggle-lock"
    name: "Excalidraw: 文本元素：原文模式（RAW）⟺ 预览模式（PREVIEW）"
  - id: "obsidian-excalidraw-plugin:scriptengine-store"
    name: "Excalidraw: 安装或更新 Excalidraw 脚本"
  - id: "obsidian-excalidraw-plugin:delete-file"
    name: "Excalidraw: 从仓库中删除所选图片（或以图像形式嵌入的 Markdown）源文件"
  - id: "obsidian-excalidraw-plugin:convert-text2MD"
    name: "Excalidraw: 转存为 Markdown 文档（并嵌入当前绘图）"
  - id: "obsidian-excalidraw-plugin:insert-link"
    name: "Excalidraw: 以链接形式插入文件"
  - id: "obsidian-excalidraw-plugin:insert-command"
    name: "Excalidraw: 插入 Obsidian 命令到当前绘图中"
  - id: "obsidian-excalidraw-plugin:insert-link-to-element"
    name: "Excalidraw: 复制所选元素的 [[file#^id]] 链接"
  - id: "obsidian-excalidraw-plugin:insert-link-to-element-group"
    name: "Excalidraw: 复制所选元素所在分组为 ![[file#^group=id]] 链接"
  - id: "obsidian-excalidraw-plugin:insert-link-to-element-frame"
    name: "Excalidraw: 复制所选画框为 ![[file#^frame=id]] 链接"
  - id: "obsidian-excalidraw-plugin:insert-link-to-element-frame-clipped"
    name: "Excalidraw: 复制所选画框（裁切）为 ![[file#^clippedframe=id]] 链接"
  - id: "obsidian-excalidraw-plugin:insert-link-to-element-area"
    name: "Excalidraw: 复制所选元素所在区域为 ![[file#^area=id]] 链接"
  - id: "obsidian-excalidraw-plugin:toggle-lefthanded-mode"
    name: "Excalidraw: 切换左手模式"
  - id: "obsidian-excalidraw-plugin:toggle-enable-context-menu"
    name: "Excalidraw: 切换是否启用上下文菜单（在移动设备上很有用）"
  - id: "obsidian-excalidraw-plugin:flip-image"
    name: "Excalidraw: 在弹出窗口中打开所选绘图的背景笔记"
  - id: "obsidian-excalidraw-plugin:duplicate-image"
    name: "Excalidraw: 复制所选图像，并分配一个不同的图像 ID"
  - id: "obsidian-excalidraw-plugin:reset-image-to-100"
    name: "Excalidraw: 重置图像尺寸为 100%"
  - id: "obsidian-excalidraw-plugin:reset-image-ar"
    name: "Excalidraw: 重置所选图像的纵横比"
  - id: "obsidian-excalidraw-plugin:open-link-props"
    name: "Excalidraw: 打开图像链接或 LaTeX 公式编辑器"
  - id: "obsidian-excalidraw-plugin:convert-card-to-file"
    name: "Excalidraw: 将“背景笔记”卡片保存到文件"
  - id: "obsidian-excalidraw-plugin:insert-active-pdfpage"
    name: "Excalidraw: 以图像形式嵌入当前激活的 PDF 页面"
  - id: "obsidian-excalidraw-plugin:crop-image"
    name: "Excalidraw: 裁剪图片并添加蒙版"
  - id: "obsidian-excalidraw-plugin:annotate-image"
    name: "Excalidraw: 在 Excalidraw 中标注图片"
  - id: "obsidian-excalidraw-plugin:insert-image"
    name: "Excalidraw: 以图像形式嵌入图片或 Excalidraw 绘图到当前绘图中"
  - id: "obsidian-excalidraw-plugin:import-svg"
    name: "Excalidraw: 导入 SVG 文件为线条（暂不支持文本元素）"
  - id: "obsidian-excalidraw-plugin:release-notes"
    name: "Excalidraw: 阅读本插件的更新说明"
  - id: "obsidian-excalidraw-plugin:tray-mode"
    name: "Excalidraw: 切换 UI 模式"
  - id: "obsidian-excalidraw-plugin:insert-md"
    name: "Excalidraw: 以图像形式嵌入 Markdown 文档到当前绘图中"
  - id: "obsidian-excalidraw-plugin:insert-pdf"
    name: "Excalidraw: 以图像形式嵌入最后激活的 PDF 页面"
  - id: "obsidian-excalidraw-plugin:universal-add-file"
    name: "Excalidraw: 嵌入文件 (Insert ANY file)"
  - id: "obsidian-excalidraw-plugin:universal-card"
    name: "Excalidraw: 插入“背景笔记”卡片"
  - id: "obsidian-excalidraw-plugin:insert-LaTeX-symbol"
    name: "Excalidraw: 插入 LaTeX 公式到当前绘图中"
  - id: "obsidian-excalidraw-plugin:toggle-excalidraw-view"
    name: "Excalidraw: 在 Excalidraw 和 Markdown 模式之间切换"
  - id: "obsidian-excalidraw-plugin:convert-to-excalidraw"
    name: "Excalidraw: 转换：空白 Markdown 文档 => Excalidraw 绘图"
  - id: "obsidian-excalidraw-plugin:convert-excalidraw"
    name: "Excalidraw: 转换： *.excalidraw => *.md"
---

# Excalidraw

**Description:** Sketch Your Mind. Edit and view Excalidraw drawings. Enter the world of 4D Visual PKM.
**Status:** Enabled
**Plugin ID:** obsidian-excalidraw-plugin

## Available Commands

Available command IDs (use execute_command for Obsidian-native commands):
- `obsidian-excalidraw-plugin:excalidraw-convert-image-from-url-to-local-file` -- Excalidraw: 从 URL 下载图片到本地
- `obsidian-excalidraw-plugin:excalidraw-unzip-file` -- Excalidraw: 解压当前 Excalidraw 文件
- `obsidian-excalidraw-plugin:excalidraw-publish-svg-check` -- Excalidraw: Obsidian Publish：搜索过期的 SVG 和 PNG 导出文件
- `obsidian-excalidraw-plugin:excalidraw-embeddable-poroperties` -- Excalidraw: Embeddable 元素设置
- `obsidian-excalidraw-plugin:excalidraw-embeddables-relative-scale` -- Excalidraw: 使元素的缩放级别等于当前绘图的缩放级别
- `obsidian-excalidraw-plugin:open-image-excalidraw-source` -- Excalidraw: 打开 Excalidraw 绘图
- `obsidian-excalidraw-plugin:excalidraw-disable-autosave` -- Excalidraw: 临时禁用自动保存功能，直到本次 Obsidian 退出（小白慎用！）
- `obsidian-excalidraw-plugin:excalidraw-enable-autosave` -- Excalidraw: 启用自动保存功能
- `obsidian-excalidraw-plugin:excalidraw-toggle-session-view-mode` -- Excalidraw: 切换所有 Excalidraw 绘图的查看模式，直到本次 Obsidian 退出
- `obsidian-excalidraw-plugin:excalidraw-download-lib` -- Excalidraw: 导出 stencil 库为 *.excalidrawlib 文件
- `obsidian-excalidraw-plugin:excalidraw-open-sidepanel` -- Excalidraw: 打开 Excalidraw 侧边面板
- `obsidian-excalidraw-plugin:excalidraw-open` -- Excalidraw: 打开已有的绘图 - 于新面板
- `obsidian-excalidraw-plugin:excalidraw-open-on-current` -- Excalidraw: 打开已有的绘图 - 于当前面板
- `obsidian-excalidraw-plugin:excalidraw-insert-transclusion` -- Excalidraw: 嵌入绘图 ![[drawing]] 到当前 Markdown 文档中
- `obsidian-excalidraw-plugin:excalidraw-insert-last-active-transclusion` -- Excalidraw: 嵌入最近编辑过的绘图 ![[drawing]] 到当前 Markdown 文档中
- `obsidian-excalidraw-plugin:excalidraw-autocreate` -- Excalidraw: 新建绘图 - 于新面板
- `obsidian-excalidraw-plugin:excalidraw-autocreate-newtab` -- Excalidraw: 新建绘图 - 于新标签页
- `obsidian-excalidraw-plugin:excalidraw-autocreate-on-current` -- Excalidraw: 新建绘图 - 于当前面板
- `obsidian-excalidraw-plugin:excalidraw-autocreate-popout` -- Excalidraw: 新建绘图 - 于新窗口
- `obsidian-excalidraw-plugin:excalidraw-autocreate-and-embed` -- Excalidraw: 新建绘图 - 于新面板 - 并嵌入到当前 Markdown 文档中
- `obsidian-excalidraw-plugin:excalidraw-autocreate-and-embed-new-tab` -- Excalidraw: 新建绘图 - 于新标签页 - 并嵌入到当前 Markdown 文档中
- `obsidian-excalidraw-plugin:excalidraw-autocreate-and-embed-on-current` -- Excalidraw: 新建绘图 - 于当前面板 - 并嵌入到当前 Markdown 文档中
- `obsidian-excalidraw-plugin:excalidraw-autocreate-and-embed-popout` -- Excalidraw: 新建绘图 - 于新窗口 - 并嵌入到当前 Markdown 文档中
- `obsidian-excalidraw-plugin:run-ocr` -- Excalidraw: OCR 整个绘图：识别涂鸦和图片里的文本并复制到剪贴板和笔记属性中
- `obsidian-excalidraw-plugin:rerun-ocr` -- Excalidraw: 重新 OCR 整个绘图：识别涂鸦和图片里的文本并复制到剪贴板和笔记属性中
- `obsidian-excalidraw-plugin:run-ocr-selectedelements` -- Excalidraw: OCR 选中的元素：识别涂鸦和图片里的文本并复制到剪贴板
- `obsidian-excalidraw-plugin:search-text` -- Excalidraw: 搜索文本
- `obsidian-excalidraw-plugin:fullscreen` -- Excalidraw: 切换全屏模式
- `obsidian-excalidraw-plugin:disable-binding` -- Excalidraw: 开启或关闭绑定
- `obsidian-excalidraw-plugin:disable-framerendering` -- Excalidraw: 开启或关闭画框渲染
- `obsidian-excalidraw-plugin:frame-settings` -- Excalidraw: 画框设置
- `obsidian-excalidraw-plugin:copy-link-to-drawing` -- Excalidraw: 复制绘图的 ![[drawing]] 链接
- `obsidian-excalidraw-plugin:disable-frameclipping` -- Excalidraw: 开启或关闭画框裁切
- `obsidian-excalidraw-plugin:export-image` -- Excalidraw: 导出为图片
- `obsidian-excalidraw-plugin:save` -- Excalidraw: 保存（同时更新嵌入了该绘图的 Markdown 文档）
- `obsidian-excalidraw-plugin:toggle-lock` -- Excalidraw: 文本元素：原文模式（RAW）⟺ 预览模式（PREVIEW）
- `obsidian-excalidraw-plugin:scriptengine-store` -- Excalidraw: 安装或更新 Excalidraw 脚本
- `obsidian-excalidraw-plugin:delete-file` -- Excalidraw: 从仓库中删除所选图片（或以图像形式嵌入的 Markdown）源文件
- `obsidian-excalidraw-plugin:convert-text2MD` -- Excalidraw: 转存为 Markdown 文档（并嵌入当前绘图）
- `obsidian-excalidraw-plugin:insert-link` -- Excalidraw: 以链接形式插入文件
- `obsidian-excalidraw-plugin:insert-command` -- Excalidraw: 插入 Obsidian 命令到当前绘图中
- `obsidian-excalidraw-plugin:insert-link-to-element` -- Excalidraw: 复制所选元素的 [[file#^id]] 链接
- `obsidian-excalidraw-plugin:insert-link-to-element-group` -- Excalidraw: 复制所选元素所在分组为 ![[file#^group=id]] 链接
- `obsidian-excalidraw-plugin:insert-link-to-element-frame` -- Excalidraw: 复制所选画框为 ![[file#^frame=id]] 链接
- `obsidian-excalidraw-plugin:insert-link-to-element-frame-clipped` -- Excalidraw: 复制所选画框（裁切）为 ![[file#^clippedframe=id]] 链接
- `obsidian-excalidraw-plugin:insert-link-to-element-area` -- Excalidraw: 复制所选元素所在区域为 ![[file#^area=id]] 链接
- `obsidian-excalidraw-plugin:toggle-lefthanded-mode` -- Excalidraw: 切换左手模式
- `obsidian-excalidraw-plugin:toggle-enable-context-menu` -- Excalidraw: 切换是否启用上下文菜单（在移动设备上很有用）
- `obsidian-excalidraw-plugin:flip-image` -- Excalidraw: 在弹出窗口中打开所选绘图的背景笔记
- `obsidian-excalidraw-plugin:duplicate-image` -- Excalidraw: 复制所选图像，并分配一个不同的图像 ID
- `obsidian-excalidraw-plugin:reset-image-to-100` -- Excalidraw: 重置图像尺寸为 100%
- `obsidian-excalidraw-plugin:reset-image-ar` -- Excalidraw: 重置所选图像的纵横比
- `obsidian-excalidraw-plugin:open-link-props` -- Excalidraw: 打开图像链接或 LaTeX 公式编辑器
- `obsidian-excalidraw-plugin:convert-card-to-file` -- Excalidraw: 将“背景笔记”卡片保存到文件
- `obsidian-excalidraw-plugin:insert-active-pdfpage` -- Excalidraw: 以图像形式嵌入当前激活的 PDF 页面
- `obsidian-excalidraw-plugin:crop-image` -- Excalidraw: 裁剪图片并添加蒙版
- `obsidian-excalidraw-plugin:annotate-image` -- Excalidraw: 在 Excalidraw 中标注图片
- `obsidian-excalidraw-plugin:insert-image` -- Excalidraw: 以图像形式嵌入图片或 Excalidraw 绘图到当前绘图中
- `obsidian-excalidraw-plugin:import-svg` -- Excalidraw: 导入 SVG 文件为线条（暂不支持文本元素）
- `obsidian-excalidraw-plugin:release-notes` -- Excalidraw: 阅读本插件的更新说明
- `obsidian-excalidraw-plugin:tray-mode` -- Excalidraw: 切换 UI 模式
- `obsidian-excalidraw-plugin:insert-md` -- Excalidraw: 以图像形式嵌入 Markdown 文档到当前绘图中
- `obsidian-excalidraw-plugin:insert-pdf` -- Excalidraw: 以图像形式嵌入最后激活的 PDF 页面
- `obsidian-excalidraw-plugin:universal-add-file` -- Excalidraw: 嵌入文件 (Insert ANY file)
- `obsidian-excalidraw-plugin:universal-card` -- Excalidraw: 插入“背景笔记”卡片
- `obsidian-excalidraw-plugin:insert-LaTeX-symbol` -- Excalidraw: 插入 LaTeX 公式到当前绘图中
- `obsidian-excalidraw-plugin:toggle-excalidraw-view` -- Excalidraw: 在 Excalidraw 和 Markdown 模式之间切换
- `obsidian-excalidraw-plugin:convert-to-excalidraw` -- Excalidraw: 转换：空白 Markdown 文档 => Excalidraw 绘图
- `obsidian-excalidraw-plugin:convert-excalidraw` -- Excalidraw: 转换： *.excalidraw => *.md

## Configuration File

Settings path: `.obsidian/plugins/obsidian-excalidraw-plugin/data.json`

To configure this plugin programmatically:
1. Read the config: read_file(".obsidian/plugins/obsidian-excalidraw-plugin/data.json")
2. Understand the settings structure and modify values as needed
3. Write changes: write_file(".obsidian/plugins/obsidian-excalidraw-plugin/data.json", updatedJSON)

Do NOT ask the user to open Settings UI. Modify data.json directly.

## Current Configuration

These are the plugin's current settings (sensitive values redacted):

```
showTabTitlebarButtons: true
copyLinkToElemenetAnchorTo100: false
copyFrameLinkByName: false
disableDoubleClickTextEditing: false
phoneFooterSafeAreaPadding: false
tabletFooterSafeAreaPadding: false
folder: Excalidraw
embedUseExcalidrawFolder: false
templateFilePath: Excalidraw/Template.excalidraw
scriptFolderPath: Excalidraw/Scripts
fontAssetsPath: Excalidraw/CJK Fonts
loadChineseFonts: false
loadJapaneseFonts: false
loadKoreanFonts: false
compress: true
decompressForMDView: false
autosave: true
autosaveIntervalDesktop: 60000
autosaveIntervalMobile: 30000
drawingFilenamePrefix: Drawing 
drawingEmbedPrefixWithFilename: true
drawingFilnameEmbedPostfix:  
drawingFilenameDateTime: YYYY-MM-DD HH.mm.ss
useExcalidrawExtension: true
cropPrefix: cropped_
annotatePrefix: annotated_
annotatePreserveSize: false
displaySVGInPreview: false
previewImageType: SVG
renderingConcurrency: 3
imageCacheRetentionDays: 30
allowImageCache: true
allowImageCacheInScene: true
displayExportedImageIfAvailable: false
previewMatchObsidianTheme: false
width: 400
overrideObsidianFontSize: false
dynamicStyling: colorful
isLeftHanded: false
desktopUIMode: tray
tabletUIMode: compact
phoneUIMode: mobile
iframeMatchExcalidrawTheme: true
matchTheme: false
matchThemeAlways: false
matchThemeTrigger: false
defaultMode: normal
defaultPenMode: never
penModeDoubleTapEraser: true
penModeSingleFingerPanning: true
penModeCrosshairVisible: true
panWithRightMouseButton: false
renderImageInMarkdownReadingMode: false
renderImageInHoverPreviewForMDNotes: false
renderImageInMarkdownToPDF: false
allowPinchZoom: false
allowWheelZoom: false
zoomToFitOnOpen: true
zoomToFitOnResize: false
zoomToFitMaxLevel: 2
zoomStep: 0.05
zoomMin: 0.1
zoomMax: 30
parseTODO: false
todo: ☐
done: 🗹
hoverPreviewWithoutCTRL: false
linkOpacity: 1
openInAdjacentPane: true
showSecondOrderLinks: true
focusOnFileTab: true
openInMainWorkspace: true
showLinkBrackets: false
syncElementLinkWithText: false
allowCtrlClick: true
forceWrap: false
pageTransclusionCharLimit: 200
wordWrappingDefault: 0
removeTransclusionQuoteSigns: true
oEmbedAllowed: false
pngExportScale: 1
exportWithTheme: true
exportWithBackground: true
exportPaddingSVG: 10
exportEmbedScene: false
keepInSync: false
autoexportSVG: false
autoexportPNG: false
autoExportLightAndDark: false
autoexportExcalidraw: false
embedType: excalidraw
embedMarkdownCommentLinks: true
embedWikiLink: true
embedPlaceholderImage: true
syncExcalidraw: false
experimentalFileType: false
experimentalFileTag: ✏️
experimentalLivePreview: true
fadeOutExcalidrawMarkup: false
loadPropertySuggestions: false
experimentalEnableFourthFont: false
experimantalFourthFont: Virgil
addDummyTextElement: false
zoteroCompatibility: false
fieldSuggester: true
enableOnloadScripts: false
enableCommandLinks: false
compatibilityMode: false
drawingOpenCount: 0
library: deprecated
library2:
  type: excalidrawlib
  source: https://github.com/zsviczian/obsidian-excalidraw-plugin/releases/tag/2.25.3
imageElementNotice: true
mdSVGwidth: 500
mdSVGmaxHeight: 800
mdFont: Cascadia
mdFontColor: Black
mdBorderColor: Black
previousRelease: 2.25.3
showReleaseNotes: true
excalidrawMasteryPromoCollapsed: false
compareManifestToPluginVersion: true
showNewVersionNotification: true
latexBoilerplate: \color{green}e=mc^2
latexPreambleLocation: preamble.sty
taskboneEnabled: false
customPens: [10 items: {...}, {...}, {...}...]
numberOfCustomPens: 0
pdfScale: 4
pdfBorderBox: true
pdfFrame: false
pdfGapSize: 20
pdfGroupPages: false
pdfLockAfterImport: true
pdfNumColumns: 1
pdfNumRows: 1
pdfDirection: right
pdfImportScale: 0.3
gridSettings:
  DYNAMIC_COLOR: true
  COLOR: #000000
  OPACITY: 50
  GRID_DIRECTION:
    horizontal: true
    vertical: true
laserSettings:
  DECAY_LENGTH: 50
  DECAY_TIME: 1000
  COLOR: #ff0000
embeddableMarkdownDefaults:
  useObsidianDefaults: false
  backgroundMatchCanvas: false
  backgroundMatchElement: true
  backgroundColor: #fff
  backgroundOpacity: 60
  borderMatchElement: true
  borderColor: #fff
  borderOpacity: 0
  filenameVisible: false
  lockedReadingMode: false
markdownNodeOneClickEditing: false
canvasImmersiveEmbed: true
aiEnabled: true
aiVerboseLogging: false
aiProviderProfiles:
  OpenAI:
    provider: openai
    baseURL: https://api.openai.com/v1
  Anthropic:
    provider: anthropic
    baseURL: https://api.anthropic.com/v1
  Google Gemini:
    provider: google
    baseURL: https://generativelanguage.googleapis.com/v1beta
  xAI:
    provider: xai
    baseURL: https://api.x.ai/v1
  OpenAI-compatible:
    provider: openai-compatible
    baseURL: https://api.openai.com/v1
aiTextModelConfigs:
  gpt-5-mini:
    providerId: OpenAI
    model: gpt-5-mini
    multimodalSupport: true
  claude-sonnet-4-5:
    providerId: Anthropic
    model: claude-sonnet-4-5
    multimodalSupport: true
  gemini-2.5-pro:
    providerId: Google Gemini
    model: gemini-2.5-pro
    multimodalSupport: true
  grok-4-fast:
    providerId: xAI
    model: grok-4-fast
    multimodalSupport: true
aiImageModelConfigs:
  dall-e-2:
    providerId: OpenAI
    model: dall-e-2
    supportedSizes: [256x256, 512x512, 1024x1024]
    supportsPromptImageTransforms: true
    supportsMaskImageEdits: true
  dall-e-3:
    providerId: OpenAI
    model: dall-e-3
    supportedSizes: [1024x1024, 1792x1024, 1024x1792]
    supportsPromptImageTransforms: false
    supportsMaskImageEdits: false
  gpt-image-1:
    providerId: OpenAI
    model: gpt-image-1
    supportedSizes: [1024x1024, 1536x1024, 1024x1536]
    supportsPromptImageTransforms: true
    supportsMaskImageEdits: true
  gpt-image-1-mini:
    providerId: OpenAI
    model: gpt-image-1-mini
    supportedSizes: [1024x1024, 1536x1024, 1024x1536]
    supportsPromptImageTransforms: true
    supportsMaskImageEdits: true
  gpt-image-1.5:
    providerId: OpenAI
    model: gpt-image-1.5
    supportedSizes: [1024x1024, 1536x1024, 1024x1536]
    supportsPromptImageTransforms: true
    supportsMaskImageEdits: true
  gpt-image-2:
    providerId: OpenAI
    model: gpt-image-2
    supportedSizes: [1024x1024, 1536x1024, 1024x1536, 2048x2048]
    supportsPromptImageTransforms: true
    supportsMaskImageEdits: true
  gemini-2.5-flash-image:
    providerId: Google Gemini
    model: gemini-2.5-flash-image
    supportedSizes: [1024x1024, 848x1264, 1264x848, 896x1200, 1200x896, 928x1152, 1152x928, 768x1376, 1376x768, 1584x672]
    supportsPromptImageTransforms: true
    supportsMaskImageEdits: false
  gemini-3.1-flash-image-preview:
    providerId: Google Gemini
    model: gemini-3.1-flash-image-preview
    supportedSizes: [56 items: 512x512, 1024x1024, 2048x2048...]
    supportsPromptImageTransforms: true
    supportsMaskImageEdits: false
  gemini-3-pro-image-preview:
    providerId: Google Gemini
    model: gemini-3-pro-image-preview
    supportedSizes: [1024x1024, 2048x2048, 4096x4096, 848x1264, 1696x2528, 3392x5056, 1264x848, 2528x1696, 5056x3392, 896x1200, 1792x2400, 3584x4800, 1200x896, 2400x1792, 4800x3584, 928x1152, 1856x2304, 3712x4608, 1152x928, 2304x1856, 4608x3712, 768x1376, 1536x2752, 3072x5504, 1376x768, 2752x1536, 5504x3072, 1584x672, 3168x1344, 6336x2688]
    supportsPromptImageTransforms: true
    supportsMaskImageEdits: false
  grok-imagine-image-quality:
    providerId: xAI
    model: grok-imagine-image-quality
    supportedSizes: [1024x1024]
    supportsPromptImageTransforms: true
    supportsMaskImageEdits: false
  grok-imagine-image-pro:
    providerId: xAI
    model: grok-imagine-image-pro
    supportedSizes: [1024x1024]
    supportsPromptImageTransforms: true
    supportsMaskImageEdits: false
aiDefaultTextModel: gpt-5-mini
aiDefaultImageGenerationModel: gpt-image-1
modifierKeyConfig:
  Mac:
    LocalFileDragAction:
      defaultAction: image-import
      rules: [4 items]
    WebBrowserDragAction:
      defaultAction: image-url
      rules: [4 items]
    InternalDragAction:
      defaultAction: link
      rules: [4 items]
    LinkClickAction:
      defaultAction: new-tab
      rules: [5 items]
  Win:
   
[...truncated -- full settings in data.json]
```
(8 sensitive field(s) redacted)

For full settings, read: `.obsidian/plugins/obsidian-excalidraw-plugin/data.json`

## Documentation

For detailed plugin documentation (commands, options, dependencies):
read_file(".vault-operator/plugin-skills/obsidian-excalidraw-plugin.readme.md")

## Usage

When the user asks for functionality related to Excalidraw:
1. Read the plugin documentation (.readme.md) to understand capabilities and dependencies
2. Read the config file (.obsidian/plugins/obsidian-excalidraw-plugin/data.json). If it does not exist, that is normal -- create it with the required settings
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
