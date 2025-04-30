---
title: 更新及重装 Zotero Connector 教程
date: 2025-04-30
---

# 更新及重装 Zotero Connector 教程

Zotero Connector 浏览器扩展是 Zotero 从网页抓取文献信息的必要工具。建议保持其为最新版本，并在遇到问题时尝试重装。

本文档将指导您如何检查 Zotero Connector 的更新、更新其内部的转换器缓存，以及在必要时卸载并重新安装 Zotero Connector。

[[TOC]]

## 检查 Zotero Connector 更新 <Badge text="初级" />

通常浏览器会自动更新扩展程序。但您也可以手动检查更新：

1.  打开浏览器的扩展管理页面：
    - **Chrome/Edge**: 点击菜单（三个点）→ 扩展 → 管理扩展。确保页面上的「开发者模式」已开启，然后点击「更新」按钮。
    - **Firefox**: 点击菜单（三横线）→ 扩展和主题 → 点击右上角的齿轮图标 → 检查更新。
    - **Safari**: Safari 扩展随 Zotero 应用更新，请确保 Zotero 应用本身是最新版本。
2.  如果发现有可用更新，请按照提示进行更新。

## 卸载并重装 Zotero Connector <Badge text="中级" />

如果更新转换器缓存后问题依旧，或者怀疑是扩展冲突导致 Zotero Connector 无法正常工作，可以尝试卸载并重新安装。

请根据您使用的浏览器，按照以下步骤操作（360、搜狗、QQ 等 Chromium 内核浏览器请参照 Chrome/Edge）：

::: details Google Chrome、 Microsoft Edge 和 Mozilla Firefox

1.  进入浏览器的扩展管理页面：

    - **Chrome**: 点击菜单（三个点）→ 扩展程序 → 管理扩展程序。
    - **Edge**: 点击菜单（三个点）→ 扩展 → 管理扩展。
    - **Firefox**: 点击菜单（三横线）→ 扩展和主题。

    ![在 Chrome 中打开管理扩展程序](../../../assets/images/uninstall-connector-chrome.jpg)

2.  找到 Zotero Connector，点击「移除」或「删除」（Firefox 可能在三个点菜单内）。

    ![在扩展中移除 Zotero Connector](../../../assets/images/uninstall-connector-chrome2.jpg)

3.  访问 [Zotero 官网下载页面](https://www.zotero.org/download/)，点击对应浏览器的「Install Connector」按钮，按照提示重新安装。

4.  安装完成后，可能需要手动将其固定到浏览器工具栏。请参考：[Zotero Connector 浏览器扩展安装教程](../../install.md#浏览器扩展-zotero-connector)。

5.  重装后，建议再次执行 [更新 Zotero Connector 的转换器缓存](tutorial-update-translators.md) 的步骤。

:::

::: details Apple Safari

Safari 的 Zotero Connector 是随 Zotero 桌面应用一起安装的。重装 Connector 需要卸载并重装 Zotero 应用本身。

**注意**：仅删除 Zotero 应用文件通常不会影响您的文献库、设置或插件。如果不放心，请先[备份 Zotero 数据](../../backup.md)。

1.  打开 Safari，点击屏幕左上角的「Safari 浏览器」菜单，选择「设置」。

    ![打开 Safari 设置](../../../assets/images/uninstall-connector-safari.jpg)

2.  在设置窗口中，切换到「扩展」选项卡。

3.  在左侧列表中找到 Zotero Connector，点击右侧的「卸载」按钮。

    ![在扩展中点击卸载](../../../assets/images/uninstall-connector-safari1.jpg)

4.  在弹出的确认窗口中，点击「在访达中显示」。

    ![在访达中显示](../../../assets/images/uninstall-connector-safari2.jpg)

5.  **完全退出 Safari 浏览器**。

6.  回到上一步打开的访达窗口（通常是「应用程序」文件夹），将 Zotero 应用拖到废纸篓。

    ![删除 Zotero 程序文件](../../../assets/images/uninstall-connector-safari3.jpg)

7.  访问 [Zotero 官网下载页面](https://www.zotero.org/download/)，下载适用于 macOS 的 Zotero 安装包（.dmg 文件）。

8.  打开 .dmg 文件，将 Zotero 图标拖到「应用程序」文件夹，完成安装。

9.  运行一次新安装的 Zotero 应用。这会自动重新安装 Safari 的 Zotero Connector 扩展。

10. 重新打开 Safari。如果 Zotero Connector 图标未出现在工具栏：

    - 回到 Safari 设置的「扩展」选项卡，确保 Zotero Connector 左侧的复选框已勾选。
    - 如果在工具栏仍看不到图标，右键点击工具栏空白处，选择「自定工具栏...」。
      ![自定义工具栏](../../../assets/images/connector-safari-button.jpg)
    - 将下方的 Zotero Connector 图标拖动到上方工具栏的期望位置。
      ![将 Zotero Connector 按钮拖至合适位置](../../../assets/images/connector-safari-button2.jpg)

11. 重装后，建议再次执行 [更新 Zotero Connector 的转换器缓存](tutorial-update-translators.md) 的步骤。

:::

## 更新/重装后的建议操作

重装 Zotero Connector 后，建议您按照 [更新 Zotero 转换器教程](tutorial-update-translators.md) 中的步骤，更新 Zotero 主程序和 Zotero Connector 中的转换器缓存，确保抓取功能正常。
