# SynapsePlayer 隐私政策

最后更新：2026-11-10

SynapsePlayer 是一个在本地运行的桌面视频播放器。本政策说明它在运行过程中如何处理你的数据。

## 总则

**SynapsePlayer 没有服务器。** 它不会把任何数据上传给本项目作者，也不会向第三方出售、共享或用于广告投放。
所有网络请求都是你的电脑与「你自己选择的数据源」之间的直接连接。

## 数据存放在哪里

播放器的全部数据都保存在你的电脑上，默认位于 `%LocalAppData%\SynapsePlayer\`：

| 数据 | 文件 | 保护方式 |
|---|---|---|
| 站点登录 Cookie | `provider-credentials.json` | 本地明文 JSON，仅本机可读 |
| Google Drive 授权令牌 | `cloud-drive-googledrive.dat` | Windows DPAPI 加密，绑定当前 Windows 用户与机器 |
| Google Drive 文件夹封面缓存 | `googledrive-folder-covers.json` | 仅含文件夹 ID 与缩略图地址，不含令牌 |
| 媒体缓存 | `Cache\Media\` | 按块缓存已播放的媒体内容 |
| 播放记录、设置、字幕 | 同目录下的 json 文件 | 本地明文 |

上述文件都不会被自动上传。删除它们即等于清除对应数据。

## 各数据源的权限范围

| 数据源 | 申请的权限 | 用途 |
|---|---|---|
| Google Drive | `drive.readonly`（只读） | 列出目录、读取视频元数据、播放原始文件。**不会修改、删除或上传任何云盘文件** |
| 站点数据源（如哔哩哔哩、YouTube） | 你登录后由站点下发的 Cookie | 访问你本就有权访问的内容 |
| 本地媒体库 | 你主动添加的本地目录 | 扫描文件名与元数据 |

播放器不会在后台扫描云盘或站点账号内容，也不会建立上传到任何地方的索引。

## 与第三方共享

不共享。除了你的电脑与你选择的数据源服务器之间的 HTTPS 请求，没有其他数据流向。
本项目不包含统计、埋点或崩溃上报组件。

## 你的控制权

| 操作 | 方式 |
|---|---|
| 撤销 Google 授权 | 访问 https://myaccount.google.com/permissions 移除本应用的访问权 |
| 清除本机凭据 | 删除 `%LocalAppData%\SynapsePlayer\` 下对应的凭据文件 |
| 清除媒体缓存 | 删除 `%LocalAppData%\SynapsePlayer\Cache\` |
| 完全移除 | 卸载播放器并删除上述目录 |

## 儿童隐私

本软件不面向儿童，也不收集任何年龄相关信息。

## 政策变更

本政策如有修改，会更新本文档顶部的日期，并在仓库提交历史中可查。

## 联系方式

问题与建议请提交到 https://github.com/alex8224/synapse-player/issues 。
