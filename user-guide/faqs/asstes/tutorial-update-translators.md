---
title: 更新 Zotero 转换器教程
date: 2025-04-30
---

# 更新 Zotero 转换器教程

Zotero 的转换器（Translators）是从网页抓取文献信息的核心组件。保持转换器为最新版本，可以确保 Zotero 能够正确识别和抓取文献信息。

本教程将指导您如何更新 Zotero 的官方转换器和中文转换器。

::: info 提醒

这里的「转换器」指的是 Zotero 从浏览器网页抓取文献信息时所需的转换器，在 Zotero 中有时也被称作是「翻译器」或「translator」。如果你遇到的是语言翻译问题（如标题翻译、摘要翻译、文献阅读中的句段翻译等），通常与本文讲的转换器（translator）无关，请参照 Translate for Zotero 插件的教程进行排查。

:::

[[TOC]]

## 方法 1：一键自动更新 <Badge text='推荐' />

### 步骤 1. 更新官方转换器

在 `Zotero 设置` 中，进入 `高级` 设置，点击下方「自动检查转换器和样式的更新」后面的 `立即更新` 按钮。更新完成后，按钮上的文字会变成 `已更新`。如果按钮上显示 `错误`，请稍等片刻再重新点击按钮尝试更新。

![更新官方转换器](../../../assets/images/update-official-translators.jpg)

::: tip 推荐保持自动更新

我们推荐保持勾选 「自动检查转换器和样式的更新」 以获得最新的官方转换器。

:::

### 步骤 2. 更新中文转换器

1. 安装/更新茉莉花插件

   茉莉花插件是一个 Zotero 中文生态增强插件，提供了中文转换器的更新服务，请确保你安装了最新版本的茉莉花插件，浏览 [茉莉花](../../plugins/jasminum.md) 了解详情。

2. 进入茉莉花插件的设置，转到 「中文转换器设置」 部分，然后点击 「立即更新」 按钮。这一按钮点一下即可，请不要短时间内连续点多次，以免出现意外错误。

   ![更新「中文转换器」](../../../assets/images/update-unofficial-translators.png)

   请耐心等待更新完成，更新结束后会有「转换器更新完成」的弹窗提示。如果更新长时间没有反应，您也可以开启一些访问国际互联网的工具后再尝试更新。更新可能会持续几分钟，取决于您的网络环境，请耐心等待。

   ![「中文转换器」更新成功](../../../assets/images/update-unofficial-translators-success.png){width=50%}

   ::: details 对于 Zotero 6 用户

   如果您使用的是 Zotero 6，茉莉花插件的设置界面会有所不同。请在茉莉花插件的设置界面中找到 「非官方维护中文转换器（翻译器）」 部分，然后点击 「更新全部」 按钮。如果您的转换器列表为空，或点击「更新全部」后本地版本的日期和最新版本的日期仍然不一致，通常意味着您的茉莉花插件版本过老，请务必确保安装了最新版本的茉莉花插件后再重试。

   Zotero 7 的正式版已经发布，由于 Zotero 6 的插件已经基本停止维护，可能会遇到兼容性问题，建议您在做好[备份](../../backup.md)后，尽快升级到 Zotero 7。

   升级 Zotero 7 正式版的步骤和常见问题的解答请阅读：[你好，Zotero 7](https://zotero-chinese.com/blog/posts/hello-zotero-7)。

   :::

   ::: info 提醒

   建议勾选「自动更新转换器」，保持转换器为最新版本。

   如果自动更新失败，您也可以手动点击「立即更新」按钮进行更新，并在转换器详情页面确认更新成功。

   :::

### 步骤 3. 更新 Zotero Connecter 的缓存

1. 更新 **每一个浏览器** 中 Zotero Connector 扩展里的转换器（translators）。

   ::: tip

   从 Zotero Connector v5.0.124 开始，官方移除了 Zotero Connector 设置里 「Advanced」->「Translators」 中的 `Update Translaors` 按钮，如果你的浏览器扩展中仍然保留 `Update Translaors` 按钮，请务必先[升级 Zotero Connector 浏览器扩展](../../install.md#浏览器扩展-zotero-connector)再进行后续操作。

   :::

   请根据您使用的浏览器点开下面相应的说明，并按照说明中的步骤操作。（360（极速）浏览器、搜狗浏览器、QQ 浏览器等基于 Chromium 等国内厂商推出的浏览器请参照 Google Chrome 的步骤操作）

   ::: details Google Chrome、 Microsoft Edge 和 Mozilla Firefox

   1. 右键点击 Zotero Connector 按钮，然后点击「选项/Preference」

      ![打开 Zotero Connector 的选项](../../../assets/images/update-translator-chrome-1.jpg)

   2. 点击「Advanced」中的「Reset Translators」按钮

      ![更新 Zotero Connector 中的 translators](../../../assets/images/update-translator-ResetTranslators.jpg)

   :::

   ::: details Apple Safari

   虽然 Zotero 目前已经支持在 Safari 中使用，但实际使用中在 Safari 中抓取失败的案例比较多。 \*\*建议使用 Microsoft Edge、Google Chrome 或 Mozilla Firefox 浏览器进行抓取。

   1. 在网页空白处点鼠标右键，然后点击「Zotero Preference」

      ![打开 Zotero Connector 的选项](../../../assets/images/update-translator-safari-1.jpg)

   2. 点击「Advanced」中的「Reset Translators」按钮

      ![更新 Zotero Connector 中的 translators](../../../assets/images/update-translator-ResetTranslators.jpg)

   :::

   ::: warning

   **这一步骤非常关键！** 请务必确保为 **每一个浏览器** 中的 Zotero Connector 扩展更新转换器！

   :::

2. 重启浏览器。

3. 此时你已经完成了转换器的更新。此时如果你的浏览器仍然不能完成对文献的识别，在确保步骤 1-2 正确的前提下，可重复几次步骤 3 。

## 方法 2：手动替换转换器文件更新 <Badge text="高级" />

::: warning 不推荐这种方法

我们推荐使用 「方法 1：一键自动更新」 完成转换器更新。手动更新下载转换器的步骤比较繁琐，且从 GitHub 下载文件时对网络环境要求较高，可能会导致下载失败。如果您因为特殊原因无法完成自动更新，才需要考虑手动更新转换器。

:::

:::: details 手动更新转换器的步骤

1. 在 Zotero →「编辑」→「设置」→「高级」→「文件和文件夹」找到自己的「数据储存位置」。点击「打开数据文件夹」快速打开你的数据文件夹。

   例如，下图中的数据储存位置就是 `D:\ZoteroDataDirectory`。

   ![数据储存位置](../../../assets/images/zotero-数据储存位置.png)

2. 找到数据文件夹中的 translators 文件夹（对上图而言就是 `D:\ZoteroDataDirectory\translators`），这里是 Zotero 转换器 的存放位置。

   ![转换器的存放位置](../../../assets/images/数据储存位置translators文件夹.png)

3. 首先，在 [Zotero 官方转换器仓库](https://github.com/zotero/translators) 下载最新的官方转换器。

   ![手动在GitHub上下载转换器](../../../assets/images/手动在github下载官方translators.png)

4. 将下载的 zip 文件解压后选择其中所有的转换器文件（.js 文件），并复制。

   ![选择所有的转换器文件](../../../assets/images/官方translators文件.png)

5. 将所有的转换器文件粘贴到第 2 步中 translators 文件夹并替换，此时已经完成 Zotero 的官方转换器文件的更新。

   ![替换旧的转换器](../../../assets/images/手动更新官方translators.png)

6. 然后，在 [Zotero translators 中文维护小组](https://github.com/l0o0/translators_CN) 下载最新的中文转换器。

![手动在GitHub上下载转换器](../../../assets/images/手动在github下载translators.png)

10. 将下载的 zip 文件解压后选择其中所有的转换器文件（.js 文件），并复制。

![选择所有的转换器文件](../../../assets/images/translators文件.png)
![选择所有的转换器文件](../../../assets/images/translators文件2.png)

11. 将所有的转换器文件粘贴到第 2 步中 translators 文件夹并替换，此时已经完成 Zotero 的中文转换器文件的更新。

![替换旧的转换器](../../../assets/images/手动更新translators.png)

12. 更新 **每一个浏览器** 中 Zotero Connector 扩展里的转换器（translators）。

::: tip

从 Zotero Connector v5.0.124 开始，官方移除了 Zotero Connector 设置里 「Advanced」->「Translators」 中的 `Update Translaors` 按钮，如果你的浏览器扩展中仍然保留 `Update Translaors` 按钮，请务必先[升级 Zotero Connector 浏览器扩展](../../install.md#浏览器扩展-zotero-connector)再进行后续操作。

:::

请根据您使用的浏览器点开下面相应的说明，并按照说明中的步骤操作。（360（极速）浏览器、搜狗浏览器、QQ 浏览器等基于 Chromium 等国内厂商推出的浏览器请参照 Google Chrome 的步骤操作）

::: details Google Chrome、 Microsoft Edge 和 Mozilla Firefox

1.  右键点击 Zotero Connector 按钮，然后点击「选项/Preference」

    ![打开 Zotero Connector 的选项](../../../assets/images/update-translator-chrome-1.jpg)

2.  点击「Advanced」中的「Reset Translators」按钮

    ![更新 Zotero Connector 中的 translators](../../../assets/images/update-translator-ResetTranslators.jpg)

:::

::: details Apple Safari

虽然 Zotero 目前已经支持在 Safari 中使用，但实际使用中在 Safari 中抓取失败的案例比较多。 \*\*建议使用 Microsoft Edge、Google Chrome 或 Mozilla Firefox 浏览器进行抓取。

1.  在网页空白处点鼠标右键，然后点击「Zotero Preference」

    ![打开 Zotero Connector 的选项](../../../assets/images/update-translator-safari-1.jpg)

2.  点击「Advanced」中的「Reset Translators」按钮

    ![更新 Zotero Connector 中的 translators](../../../assets/images/update-translator-ResetTranslators.jpg)

:::

::: warning

**这一步骤非常关键！** 请务必确保为 **每一个浏览器** 中的 Zotero Connector 扩展更新转换器！

:::

此时你已经完成了转换器的更新，此时如果你的浏览器仍然不能完成对文献的识别，请再次更新 **每一个浏览器** 中 Zotero Connector 扩展里的转换器（translators），并重启浏览器。

::::

## 仍然无法抓取条目怎么办？

如果您在更新转换器后仍然无法抓取条目，请阅读以下教程进行排查：

- [检查 Zotero 转换器更新是否成功](troubleshooting-translator-update.md)
- [Zotero Connector 抓取条目失败常见问题](../add-item//troubleshooting-browser.md)
