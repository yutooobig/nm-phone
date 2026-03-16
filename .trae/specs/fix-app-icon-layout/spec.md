# 修复应用图标布局问题 Spec

## Why
应用图标都堆在左上角，因为 `.app-icon` 使用了 `position: absolute` 但没有设置具体的 `top` 和 `left` 定位值。需要：
1. 将 `#app-page-3` 的内容合并到 `#app-page-2`
2. 为所有应用图标添加网格布局定位
3. 删除不需要的第二页和相关滑块结构

## What Changes
- 将 `#app-page-3` 中的应用图标（时光记事簿、直播）移动到 `#app-page-2`
- 删除 `#app-page-3` 整个div
- 删除页面指示器 `#home-page-indicator`
- 修改 `#app-pages-slider` 宽度为100%（不再需要200%）
- 为所有应用图标添加CSS定位样式，使用网格布局

## Impact
- Affected code: `index.html` 中的 HTML 结构和 CSS 样式部分

## ADDED Requirements
### Requirement: 单页应用图标布局
所有应用图标应该在一个页面上以网格形式均匀分布。

#### Scenario: 主页布局
- **WHEN** 用户打开应用
- **THEN** 所有应用图标在一个页面上以网格形式排列
- **AND** 图标之间有适当的间距
- **AND** 图标不重叠
