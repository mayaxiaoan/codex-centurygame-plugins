# CenturyGame班用插件

供同事共享和测试的 Codex 插件市场。此仓库只保存轻量目录和说明；安装具体插件时才获取对应插件仓库。

## 添加市场

在 Codex 的“插件 → 添加 → 添加插件市场”填写：

- 来源：`https://github.com/mayaxiaoan/codex-centurygame-plugins.git`
- Git 引用：`main` 或留空。
- 稀疏路径：留空。本仓库不包含大体积运行环境。

添加后选择“CenturyGame班用插件”，安装所需插件，并按提示重启 Codex。

## 插件目录

| 插件 | 平台 | 功能与安装内容 |
| --- | --- | --- |
| [重置卡防过期提醒](https://github.com/mayaxiaoan/codex-reset-card-reminder-windows) | Windows x64 | 按剩余时长通知、可选自动使用；内置 Node.js；使用系统通知组件，无需安装现代 .NET。 |

## 从旧市场迁移

市场内部标识已从 reset-guard-creator-local 改为 centurygame-plugins，界面显示名仍为“CenturyGame班用插件”。完整安装 ID 因而改为 codex-reset-guard-creator@centurygame-plugins。已有安装请先卸载旧 ID 的插件、移除旧市场，再添加本仓库并安装 1.6.3，避免两个后台同时运行。个人数据目录 Documents/Codex/ResetGuardCreator、现有设置和通知标识保持不变，不要删除该目录。全新安装直接添加本仓库即可。

## 提交其他插件

每个插件使用独立、稳定的内部名称，在自己的仓库维护源码、运行内容、说明和版本。在 .agents/plugins/marketplace.json 的 plugins 数组增加目录条目，source 使用 url（插件在仓库根目录）或 git-subdir（插件在子目录），指定来源 URL、ref 和必要的 path。
请始终提供 installation、authentication 与 category；不要修改已有插件的内部名称。提供支持平台、权限、依赖、测试结果和隐私说明，通过 Pull Request 更新目录。
本目录及其引用仓库公开可读，不得提交账号凭证、个人状态、内部秘密或未获授权的公司资料。公开仓库不是访问控制；仅供当前共享测试，未通过官方公开插件目录审核。

当前重置卡正式版为 **1.6.3**，目录固定到经过验证的提交；1.6.0 已因脚本通知快捷方式告警撤回。1.6.1 使用约50KB标准EXE和Windows自带.NET Framework，已完成回归测试、Defender文件扫描及本机通知验证，不需放行被隔离的旧快捷方式。发布新版本时应先完成验证，再更新目录中的 sha。

## 安装前展示信息

跨仓库插件条目必须在 plugins[] 对象中提供顶层 interface（displayName、shortDescription、longDescription、developerName、websiteURL 等），用于在未下载插件包时展示信息。仅在插件包内填写 extensions.com.openai.interface 不足以给安装前的跨仓库目录提供这些字段。当前客户端会清除跨仓库预览的本地图片路径，故安装前可能仍显示默认图标；安装后读取真实包内图标。不要为了预览图标把运行环境放回市场仓库。

市场添加提示和缓存目录使用内部标识 centurygame-plugins，展示标题使用 CenturyGame班用插件。这两个名称承担不同用途，无需让目录使用中文。1.6.2 同步修正通知中的打开插件链接；通知 EXE 仍为 50,176 字节，不新增运行环境。

1.6.3 修复旧后台阻止新页面和原生设置加载的问题：使用保留设置的升级接口正常退出旧后台，串行接管且不降级较新兼容后台。时长设置、提醒会话和去重记录保留，通知 EXE 和运行环境不变。
