# SynapsePlayer 文档

本仓库只存放 SynapsePlayer 的对外文档，不含源码。

SynapsePlayer 是一个在本地运行的 Windows 桌面视频播放器（.NET 8 / WPF），
把多个在线数据源与网盘内容统一到一个界面里浏览与播放。

## 主要能力

| 能力 | 说明 |
|---|---|
| 多数据源 | 站点数据源以插件形式加载，互不干扰 |
| 网盘直连 | Google Drive：目录树浏览、搜索、原始文件直接播放 |
| 本地媒体库 | 扫描本地目录、刮削元数据 |
| 播放 | 内置 mpv 引擎，支持硬件解码、字幕、弹幕、进度记忆 |
| 媒体缓存 | 按块缓存远程媒体，支持拖动进度条 |

## Google Drive 数据源

在播放器的数据源菜单里选择 **Google Drive**：

1. 首次进入时用浏览器完成 Google 账号授权，只申请只读权限
2. 授权后可浏览云盘目录、搜索视频、直接播放原始文件
3. 播放走本地中继，支持 Range 请求与拖动

## 隐私

SynapsePlayer 没有服务器，不上传任何数据。详见 [隐私政策](PRIVACY.md)。

## 反馈

问题与建议请提交到 https://github.com/alex8224/synapse-player/issues 。
