# 重写主题设置为黑白切换模式 Spec

## Why
当前的主题色滑动调节功能失效，改了也没有变化。需要完全重写主题设置功能，改为简单的黑白两种模式切换，不再使用滑动调节。

## What Changes
- 删除色相和明度滑块
- 添加"浅色模式"和"深色模式"两个切换按钮
- 重写CSS变量，使用固定的黑白两套颜色值
- 添加主题切换的JavaScript逻辑

## Impact
- Affected code: `index.html` 中的 HTML 设置面板、CSS 变量和 JavaScript 逻辑

## ADDED Requirements
### Requirement: 黑白主题切换
用户可以在浅色模式和深色模式之间切换。

#### Scenario: 切换主题
- **WHEN** 用户点击"深色模式"按钮
- **THEN** 界面变为深色背景、浅色字体
- **AND** 设置被保存到localStorage

#### Scenario: 切换回浅色模式
- **WHEN** 用户点击"浅色模式"按钮
- **THEN** 界面变为浅色背景、深色字体
- **AND** 设置被保存到localStorage
