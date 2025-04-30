---
title: 从网页抓取条目常见问题
date: 2025-04-30
---

# 从网页抓取条目常见问题

当您无法从特定网站保存正确且完整的元数据时，很可能是因为该页面没有对应的 Zotero 转换器支持，或者网站页面布局最近发生了变化，需要更新 Zotero 的转换器才能继续正常识别数据。此外，网络状况、浏览器和插件的版本等问题也可能导致 Zotero Connector 无法正常工作。

如果您在网页浏览器中使用 Zotero Connector 保存条目信息时遇到问题，请参照本文档进行故障排除。

[[TOC]]

## 初步检查 <Badge text="初级" />

1.  **检查 Zotero Connector 是否已安装并启用**：

如果您在浏览器工具栏中根本看不到「保存到 Zotero」按钮，请确保您已在浏览器中**安装了 Zotero Connector**。Zotero Connector 应列在浏览器的扩展程序窗格中。您可以阅读 [Zotero Connector 浏览器扩展安装教程](../../install.md#浏览器扩展-zotero-connector) 安装相应的 Zotero Connector。如果扩展已安装但不可见，您可能需要根据 [Zotero Connector 浏览器扩展安装教程](../../install.md#浏览器扩展-zotero-connector) 中的步骤将其固定到工具栏。

2.  **检查是否为支持的网站**：

如果您只看到灰色的网页图标，请**确保您正在查看的是受支持的网站**。通常来说，国外常见的学术搜索引擎和数据库都可以正常抓取条目（例如 Google Scholar、PubMed、IEEE Xplore、SpringerLink）。对于中文文献，可以访问「[Zotero 中文转换器](https://zotero-chinese.com/translators/)」查看支持的网站列表。学校或机构图书馆自行搭建的私有数据库或镜像站可能无法正常抓取条目。

3.  **前往文献详情页抓取**：

在「文献搜索」界面或「全文阅读」界面进行条目抓取时非常容易失败。建议您在文献的**详情页**进行条目的抓取。

::: details 典型的详情页示例

![文献详情页](../../../assets/images/update-translators-文献详情页1.png)

![文献详情页](../../../assets/images/update-translators-文献详情页2.png)

:::

4.  **重新加载页面并确保完全加载**：

如果您正在查看受支持的网站，请**尝试重新加载页面**，并**确保页面已完全加载**。如果页面上的某些内容卡住了，按浏览器的停止按钮或按键盘上的 Esc 键可能会有所帮助。如果您在访问国外的网站，您也可能需要借助一些工具来加速访问。

5.  **重启浏览器**：

如果所有网站上都出现灰色网页图标，请**尝试重新启动浏览器**。

6.  **打开 Zotero 桌面程序**：

如果您没有打开 Zotero 程序，请**尝试在保存前打开 Zotero**。Zotero Connector 需要在 Zotero 程序打开是才能将条目数据保存到您电脑中的本地 Zotero 数据库中。

7.  **检查 Zotero Connector 更新**：

从浏览器的扩展程序窗格中**检查 Zotero Connector 更新**，或重装 Zotero Connector 浏览器插件。详细教程请参考 [更新 Zotero Connector](../asstes/tutorial-reinstall-connector.md)。

8.  **检查浏览器版本**：

确保您拥有**最新版本的浏览器**。详细教程请参考 [更新网页浏览器版本](../asstes/tutorial-update-browser.md)。

9.  **检查 Zotero 版本**：

确保您的 Zotero 桌面程序是**最新版本**。详细教程请参考 [更新 Zotero 桌面程序](../asstes/tutorial-update-zotero.md)。

10. **更新 Zotero 转换器**：

网站经常更改其结构，这可能会破坏 Zotero 识别数据的能力。请按照[更新 Zotero 转换器](../asstes/tutorial-update-translators.md)教程中的步骤操作。

11. **检查已知转换器问题**：

查看[已知转换器问题](../asstes/blog-known-translator-issues.md)文档，了解您尝试保存的网站上是否已报告问题。

12. **检查 Zotero Connector 使用的转换器**：

将鼠标悬停在「保存到 Zotero」按钮上。工具提示会显示 Zotero 将用于您正在查看的页面的转换器（如果有）。如果显示的转换器与您当前访问的网站不一致，可能是当前网站不支持抓取，或需要下载/更新支持抓取当前网站的转换器（详见 [更新 Zotero 转换器](../asstes/tutorial-update-translators.md)）。

::: info 提醒

请注意，「Web Page」、「Embedded Metadata」、「DOI」和「COinS」是通用转换器，Zotero 可能无法从所有出现这些转换器的网站上保存完整的元数据或 PDF。当前网站专用的主转换器出现问题问题，或没有支持抓取当前网站的转换器时，可能会导致使用通用转换器。

:::

13. **检查 Zotero Connector 权限**：

确保您已授予 Zotero Connector **访问所有网站的权限**。在 Chrome 或 Edge 中，请打开您需要抓取的页面，右键单击「保存到 Zotero」按钮，选择「该扩展程序可以读取和更改网站数据」，并确保设置为「在所有网站上」。在 Safari 中，转到 Safari 设置的「网站」选项卡，在「扩展」下选择 Zotero Connector，并确保「对于其他网站」设置为「允许」。

## 进阶排查 <Badge text="中级" />

1.  **检查扩展冲突**：

如果您在多个网站上持续遇到 Zotero Connector 无法工作的问题，或抓取到的文献信息有误，可能是与其他浏览器扩展冲突。请尝试**禁用除 Zotero Connector 之外的所有扩展**。如果这解决了问题，请逐个重新启用扩展，直到找到冲突，然后在 [Zotero 论坛](https://forums.zotero.org/)上报告该问题。

2. **检查转换器是否更新成功**：

   如果禁用所有其他插件后仍然抓取失败，可能是转换器更新时出现问题。请按照[检查转换器是否更新成功](../asstes/troubleshooting-translator-update.md)教程中的步骤操作。

3. **重置 Zotero 转换器**：

在极少数情况下，如果您在大量网站上都看到网页图标或保存失败，则可能是本地转换器文件夹存在问题。请按照[重置 Zotero 转换器](../asstes/tutorial-reset-translators.md)教程中的步骤操作。

4.  **检查数据文件夹状态**：

如果您将 Zotero 的数据文件夹放在了网盘同步目录中，可能会导致转换器更新失败。请参考[检查 Zotero 数据文件夹状态](../asstes/troubleshooting-check-data-directory.md)教程进行检查和处理。

## 仍然无法解决？

### 使用其他添加条目的方式 <Badge text="初级" />

如果以上所有操作都未能解决你遇到的抓取问题，可能你访问的网页目前无法通过 Zotero Connector 抓取文献信息。你可以尝试换其他网站进行抓取，或者使用 [通过附件添加条目](../../add-items.md#通过附件添加条目-推荐)、[由通用格式的引用信息导入](../../add-items.md#由通用格式的引用信息导入-通用方法) 以及 [手动创建条目](../../add-items.md#手动创建条目-万能方法) 等添加条目方式。详细操作步骤请阅读 [添加条目教程](../../add-items.md) 。

### 问题反馈

如果以上所有解决方案都无法解决您的问题，我们需要更多信息来进一步调试您的问题。请在 [Zotero 论坛](https://forums.zotero.org/)上创建一个新帖子（如果您已经创建了帖子，请使用现有帖子），并提供以下信息：

- **无法正常工作的页面的完整 URL**（即使所有页面都无法工作，也请提供一个示例）
- 重新加载页面并尝试保存时，来自 Zotero Connector 的[调试 ID](https://www.zotero.org/support/debug_output#zotero_connectors_firefox_chrome_and_safari)；或者，如果您只看到网页图标，则提供重新加载页面时的调试 ID。
- 尝试保存时弹出窗口中显示的内容（例如，「正在保存到我的文库」或「正在保存到 Zotero.org」）
- 如果适用，请提供前面步骤中确定的**转换器名称**。
