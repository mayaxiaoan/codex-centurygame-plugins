# CenturyGame班用插件

Codex 插件集合。在 Codex 添加此市场后，可从目录中选择需要的插件。

## 添加市场

在 Codex 的“插件 → 添加 → 添加插件市场”填写：

- 来源：`https://github.com/mayaxiaoan/codex-centurygame-plugins.git`
- Git 引用：`main` 或留空。
- 稀疏路径：留空。

添加后选择 **CenturyGame班用插件**，安装所需插件，并按客户端提示完成安装。

## 插件目录

| 插件 | 详情 |
| --- | --- |
| 重置卡防过期提醒 | [查看插件介绍、安装说明与更新记录](https://github.com/mayaxiaoan/codex-reset-card-reminder-windows) |

各插件的功能、支持平台、依赖、使用说明及版本记录，请查看对应插件页面。

## 提交与维护插件

本仓库维护市场目录 `.agents/plugins/marketplace.json`。每个插件在独立仓库维护源码、运行内容和文档，通过 Pull Request 添加或更新目录条目。

- 为插件使用独立且稳定的内部名称，并提供名称、简短介绍和插件页面链接。
- 填写来源仓库、插件路径、安装与认证策略以及分类；发布条目固定到经过验证的提交。
- 功能介绍、安装和升级说明、依赖、权限、隐私说明及测试结果维护在插件自己的仓库中。
- 更新插件时先验证对应版本，再更新市场目录中的提交引用。

市场内部标识为 `centurygame-plugins`，在 Codex 中显示为 **CenturyGame班用插件**。

本仓库及其引用仓库公开可读。请勿提交账号凭证、个人状态或未获授权的公司资料。当前用于共享测试，未通过官方公开插件目录审核。
