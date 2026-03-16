# 修复图标居中问题 Spec

## Why
应用图标向右歪，不居中。原因是网格布局缺少 `justify-items: center` 属性，导致图标在网格单元格内没有居中对齐。

## What Changes
- 为 `.app-page` 添加 `justify-items: center` 属性，让图标在网格单元格内居中

## Impact
- Affected code: `index.html` 中的 CSS 样式部分

## ADDED Requirements
### Requirement: 图标居中对齐
应用图标应该在网格单元格内居中对齐。

#### Scenario: 主页布局
- **WHEN** 用户打开应用
- **THEN** 应用图标在网格单元格内居中显示
- **AND** 整体布局整齐美观
