---
title: 从备份中恢复 Zotero 数据
date: 2025-04-13
---

# 从备份中恢复 Zotero 数据

本教程将指导您如何从各种备份中恢复 Zotero 数据，包括同步备份、手动备份、自动备份等多种情况。

[[TOC]]

::: warning

在进行任何恢复操作前，请确保 Zotero 已经关闭。在 Zotero 运行时修改数据文件可能会导致数据损坏。

:::

::: tip 提醒

在对数据文件夹进行任何操作之前，都建议您先对数据文件夹进行备份，以备不时之需。备份的步骤详见：[Zotero 备份教程](../backup)。

:::

::: danger

无论你选择何种同步方案，也无论基于何种原因，切勿将 Zotero 的 `数据存储位置/Data Directory` 自定义为任何网盘的同步文件夹中 （包括 iCloud），也切勿使用任何网盘/同步盘的备份功能直接同步/备份这一目录!（包括但不限于直接使用坚果云的官方客户端直接同步备份这一文件夹）

这样做在某些情况下可能会导致你的 Zotero 数据库损坏，带来严重的问题！官方对于这一问题的说明见这两篇文章：

- [How can I access my library from multiple computers?](https://www.zotero.org/support/sync#alternative_syncing_solutions)
- [Can I store my Zotero data directory in a cloud storage folder?](https://www.zotero.org/support/kb/data_directory_in_cloud_storage_folder)

如果您已经将 Zotero 数据文件夹直接同步到网盘中，请您做好[备份](../backup#手动备份)，根据 [自定义数据文件夹](../faqs/custom-data-directory) 的教程将数据文件夹迁移到本地的其他位置，且确保未使用任何工具直接同步这一数据文件夹。

:::

## 使用 Zotero 同步恢复数据 <Badge text="初级" />

如果您更换了新设备，或重新安装了系统（本地库为空），且之前正确配置了 [Zotero 数据和文件同步](../sync) 功能并进行了完整的同步，您可以通过同步从在线库恢复您的数据。

1. **验证在线库数据完整性**

   首先访问 [Zotero 官网](https://www.zotero.org/user/login) 登录您的账户，然后点击页面顶部的 `Web Library` 进入在线文献库，确认在线库中的数据是否完整且正确。

   ::: details 如果您使用「WebDAV 同步」或「Attanger/ZotMoov + 同步盘」方案同步附件...

   如果您使用了「WebDAV 同步」或「Attanger/ZotMoov + 同步盘」方案同步附件，由于附件未同步在 Zotero 官方存储空间，您会在在线库中看到附件的文件名，但无法下载和查看附件，这是正常的。

   您可能需要前往 WebDAV 网盘或同步盘服务商的网页端检查附件是否完整。一般来说，您可以通过网盘中附件存储文件夹占用的空间大小来粗略判断附件同步是否完整。

   - **如果您使用的是 WebDAV 同步**：

     你可以检查 WebDAV 网盘中 `zotero` 文件夹中 `zip` 压缩包的数量，每个 `zip` 中会存放一个附件文件。通常来说，`zip` 应与 Zotero 中存储的各类附件的总数一致。

     您还可以将比较 WebDAV 网盘中 `zotero` 文件夹的大小与 Zotero 数据目录中 `storage` 文件夹的大小进行比较，来判断附件同步是否完整。由于 WebDAV 同步时会将附件压缩成 `zip` 压缩包，实际占用空间可能略小于 Zotero 数据目录中 `storage` 文件夹的大小。

   - **如果您使用的是 Attanger/Zotmoov + 同步盘**：

     您可以直接检查个文件夹中文件的数量，来判断附件是否齐全。

   :::

1. **设置同步**

   设置 Zotero 的 [数据同步](../sync#数据的同步) 和 [文件同步](../sync#文件的同步)，操作步骤详见：[Zotero 同步](../sync)。

1. **开始同步**

   点击 Zotero 界面上的「同步」按钮，Zotero 将从服务器下载您的库。

::: info

Zotero 只同步明确的删除操作，因此仅同步一个空库不会覆盖服务器数据，除非您手动删除了条目。

:::

::: details 如果您电脑上的本地 Zotero 数据库中有内容...

如果您的本地 Zotero 库有内容，但想用在线库中的数据覆盖它：

1. 关闭 Zotero。
2. 将旧的数据库复制到其他地方备份，以备不时之需。
3. 删除旧 Zotero 数据目录中的所有文件和文件夹，只保留一个空的数据目录文件夹。（如果您已将旧数据目录文件夹剪切到其他地方，您也可以在原位置新建一个同名文件夹）。
4. 重新打开 Zotero 并设置同步。操作步骤详见：[Zotero 同步](../sync)。
5. 开始同步。

:::

## 从本地备份中恢复数据

### 从完整手动备份恢复数据 <Badge text="中级" />

如果您有 Zotero 数据目录的手动 [备份](../backup)，可以用它替换当前的数据目录来恢复您的库。

1. **暂时禁用同步**

   如果您之前设置了同步，请在 Zotero 的 `编辑` → `设置` → `同步` 中，取消选中 `自动同步` 选项。这样可以防止 Zotero 在操作过程中自动同步。

2. **查看当前数据目录位置**

   打开 Zotero 的 `编辑` → `设置` → `高级` → `文件和文件夹` ，记下 `数据存储位置` 的路径（默认是您的用户文件夹中的 `Zotero` 目录）。

3. **打开数据目录**

   点击 `打开数据文件夹` 按钮，打开当前数据目录（目录中包含 `zotero.sqlite` 等文件和 `storage` 等子目录）。

4. **备份当前数据目录**

   关闭 Zotero，进入数据目录的上级文件夹，将当前数据目录重命名为 `Zotero-Old`。

5. **替换为备份数据**

   将您的备份数据目录复制到原来的位置（例如，复制到重命名前的 `Zotero` 位置，并将新复制过来的目录重命名为 `Zotero`）。

6. **重启 Zotero 并处理同步**

   重新启动 Zotero，您应该能看到备份版本的库。如果不需要的更改已经同步，请参照下面 [从备份恢复并覆盖已同步的更改](#从备份恢复并覆盖已同步的更改) 中的方法处理。

7. **重新启用同步**

   确认恢复成功后，在 Zotero 的 `编辑` → `设置` → `同步` 中，重新选中 `自动同步` 选项，启用自动同步。恢复成功后，您可以删除 `Zotero-Old` 文件夹，直到确认恢复的数据无误。

### 从数据库自动备份恢复数据 <Badge text="中级" />

如果您在使用 Zotero 时犯了错误（例如，意外删除大量条目），可以尝试恢复到最近的自动备份。

::: info

自动备份只包含数据库（文献条目信息、笔记、附件、标签、分类），不包含附件文件。

:::

1. **暂时禁用同步**

   如果您之前设置了同步，请在 Zotero 的 `编辑` → `设置` → `同步` 中，取消选中 `自动同步` 选项。这样可以防止 Zotero 在操作过程中自动同步。

2. **查找自动备份文件**

   打开您的 Zotero 数据目录，找到里面所有文件名开头为 `zotero.sqlite` 且后缀名为 `.bak` 的文件（如：`zotero.sqlite.bak`）。这些文件是 Zotero 的自动备份文君，文件的修改时间可能有助于确定哪个文件包含您要恢复的数据。建议先将这些 `.bak` 文件复制到其他位置备份一下，以备不时之需。

3. **替换数据库文件**

   关闭 Zotero。在数据目录中，将 `zotero.sqlite` 重命名为 `zotero.sqlite.old`，然后将选定的 `.bak` 文件之一重命名为 `zotero.sqlite`。

4. **重启 Zotero 并处理同步**

   重新启动 Zotero，您应该能看到备份版本的库。如果不需要的更改已经同步，请参照下面 [从备份恢复并覆盖已同步的更改](#从备份恢复并覆盖已同步的更改) 中的方法处理。

5. **重新启用同步**

   确认恢复成功后，在 Zotero 的 `编辑` → `设置` → `同步` 中，重新选中 `自动同步` 选项，启用自动同步。保留 `zotero.sqlite.old` 和您的 `.bak` 文件备份，直到确认所有数据都完好无损。

## 从备份恢复并覆盖已同步的更改 <Badge text="中级" />

如果您不小心在 Zotero 库中进行了不需要的更改并已同步到在线库，您可以使用本地备份恢复数据并覆盖在线更改。

1. **暂时禁用自动同步**

   在 Zotero 的 `编辑` → `设置` → `同步` 中，取消选中 `自动同步` 选项。这样可以防止 Zotero 在操作过程中自动同步。

2. **从备份恢复数据**

   按照前文 [从本地备份中恢复数据](#从本地备份中恢复数据) 中的步骤恢复本地数据库。

3. **处理潜在的同步冲突**

   恢复数据后，如果直接同步，在线库中的更新数据会替换您刚恢复的数据。根据情况选择以下方法之一：

   - **恢复少量删除的条目或笔记**：右键点击并选择「创建条目副本」创建副本，这样同步后新副本会保留。

   - **恢复删除的分类**：重复创建一个新的分类，并将条目从旧分类拖到新分类。同步时，旧分类将被删除，但新分类会保留。

   - **恢复大量更改**：使用「替换在线库」功能强制 Zotero 上传本地库版本，覆盖之前同步的更改。这需要在 Zotero 中点击 `编辑` → `设置` → `同步`，然后在 `重置` 中点击 `显示重置选项` 按钮，然后在「重置」界面中选中 `替换在线文献库`，最后点击 `重置...` 按钮。请注意，这将使用本地数据强制覆盖在线库中的所有数据。

4. **恢复自动同步**

   确认恢复成功后，重新启用「自动同步」选项。

## 降级 Zotero 时从升级备份恢复数据 <Badge text="高级" />

当您升级到新版本的 Zotero 时，系统会自动备份您的数据库。如果需要降级到低版本 Zotero，可以使用这些备份。

:::: details 如何降级 Zotero 并恢复数据

1. **查找升级备份文件**

   打开您的 Zotero 数据目录，升级备份通常是数据目录中编号最高的 `zotero.sqlite.[数字].bak` 文件。

2. **备份当前数据目录**

   在进行任何更改前，建议备份整个 Zotero 数据目录。备份教程详见：[Zotero 备份教程](../backup)。

3. **替换数据库文件**

   安装旧版 Zotero，关闭程序，用 `zotero.sqlite.[最高编号].bak` 替换数据目录中的 `zotero.sqlite`，然后重启 Zotero。

   ::: warning

   如果您尝试在旧版 Zotero 中打开升级后的数据库，Zotero 会显示错误。请关闭 Zotero 并按上述方法替换 `.sqlite` 文件。

   :::

4. **同步更新**

   如果您使用了同步功能，Zotero 将从在线库中同步自上次使用旧数据库以来的所有更改。

   ::: tip

   如果您没有使用同步功能，可能需要将数据库升级后添加的条目导出为 Zotero RDF 格式，然后再导入到早期版本中。按「添加日期」排序您的库可能有助于找到这些条目。

   :::

::::

## 找不到 Zotero 数据的解决方案

如果打开 Zotero 发现库为空或缺少大量数据，可能有几种原因：

1. **数据库文件损坏或丢失**

   可能是 `zotero.sqlite` 文件被意外删除或损坏。检查数据目录中是否有较大的 `zotero.sqlite.bak` 文件或其他备份。

2. **Zotero 查找数据的位置错误**

   Zotero 可能在错误的位置查找数据。检查「编辑」→「设置」→「高级」→「文件和文件夹」中的数据目录路径是否正确。

如果尝试以上方法后仍无法找到您的数据，可能需要：搜索计算机上的其他位置，寻找包含 `zotero.sqlite` 的其他文件夹。在找到合适的备份文件后，参照 [从本地备份中恢复数据](#从本地备份中恢复数据) 的步骤进行恢复。

## 仍然无法解决？

如果上面的步骤均无法解决您的问题，您可以阅读官方文档：[Restoring Your Zotero Data From a Backup - Zotero Documentation](https://www.zotero.org/support/zotero_data#restoring_your_zotero_data_from_a_backup)，了解更多细节和解决方案。

如果您确实无法成功恢复数据，您可以前往 [Zotero 官方论坛](https://forums.zotero.org/) 发帖提问寻求帮助。
