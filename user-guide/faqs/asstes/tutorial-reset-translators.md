---
title: 重置 Zotero 转换器教程
date: 2025-04-30
---

# 重置 Zotero 转换器教程

在极少数情况下，如果您在大量网站上都看到灰色的网页图标，或者在所有网站上保存都失败，则可能是 Zotero 或 Zotero Connector 内部缓存的转换器（Translators）文件存在问题。此时，可以尝试重置转换器。

::: tip 注意

这通常不是常规的故障排除步骤。在执行此操作之前，请确保您已经尝试过[更新 Zotero 转换器](tutorial-update-translators.md)和[重装 Zotero Connector](tutorial-reinstall-connector.md)。

:::

[[TOC]]

## 重置 Zotero 主程序的转换器 <Badge text="中级" />

此操作将删除 Zotero 数据文件夹内 `translators` 文件夹中的所有转换器文件，并在下次更新时重新从官方和（如果安装了茉莉花插件）中文源下载。

1.  打开 Zotero 桌面程序。

2.  点击菜单栏中的「编辑」→「设置」（macOS 上是「Zotero」→「设置」）。

3.  切换到「高级」（Advanced）选项卡。

4.  点击「文件和文件夹」（Files and Folders）子选项卡。

5.  找到「数据文件夹位置」（Data Directory Location）下的「数据库维护」（Database Maintenance）部分。

6.  点击「重置转换器…」（Reset Translators...）按钮。

    ![重置 Zotero 主程序的转换器](../../../assets/images/zotero-reset-translator.png)

7.  在弹出的确认对话框中点击「确定」。

## 重置后的必要操作：更新转换器 <Badge text="重要" />

重置转换器后，Zotero 主程序和 Connector 中的转换器文件可能已被清空或恢复到初始状态。**必须** 重新执行更新操作，才能获取最新的转换器文件。

请按照 [更新 Zotero 转换器教程](tutorial-update-translators.md) 中的步骤，更新 Zotero 主程序和 Zotero Connector 中的转换器缓存，确保抓取功能正常。
