# 修复主页内容显示问题 Spec

## Why
删除锁屏页面后，主页应用图标区域（app-page-2）不可见，只显示底部dock栏的三个图标。原因是 `#app-pages-container` 的CSS样式设置了 `opacity: 0`，这是之前锁屏功能的遗留样式。

## What Changes
- 移除 `#app-pages-container` 的 `opacity: 0` 样式，或将其改为 `opacity: 1`
- 确保主页应用图标区域正常显示

## Impact
- Affected code: `index.html` 中的 CSS 样式部分

## ADDED Requirements
### Requirement: 主页内容可见性
系统应该正常显示主页的应用图标区域，包括世界书、交换日记、音乐库、API设置等应用图标。

#### Scenario: 主页加载
- **WHEN** 用户打开应用
- **THEN** 主页应该显示所有应用图标（世界书、交换日记、音乐库、API设置、我、更换壁纸、视奸、记账等）
- **AND** 底部dock栏显示"聊天、动态、见面"三个图标
