# 微语视频会议

企业级、安全、可自托管的视频会议解决方案，面向团队与社区，基于稳定成熟的 Jitsi 平台构建。

## 概述

微语视频会议提供基于浏览器的一键开会体验，支持高清音视频、屏幕共享与会议协作。Jitsi 负责实时音视频媒体层；用户系统、认证、角色/权限与房间策略等业务能力由 微语 服务器提供（https://github.com/Bytedesk/bytedesk）。

## 功能特性

- 纯浏览器参会，无需安装客户端
- 高清音视频与自适应码率
- 屏幕共享（全屏/窗口/标签页）
- 会议聊天、表情/举手互动
- 等候室、房间密码、主持人管控
- 可选录制与直播（通过 Jibri/RTMP）
- 分组讨论与成员管理
- 跨桌面与移动端浏览器可用

## 适用场景

- 团队例会、项目评审与同步沟通
- 客户演示、面试与培训
- 社区活动、线上分享与 Webinar

## 部署与使用（概览）

生产部署通常包含两部分：

1) 自托管 Jitsi（媒体层）：
	- 按官方指南部署 Jitsi（Prosody、Jicofo、JVB，可选 Jibri）：https://jitsi.github.io/handbook/docs/devops-guide/devops-guide-quickstart
	- 配置域名、证书、TURN/ICE，以及录制/直播能力（如需）。

2) Bytedesk 服务器（业务层）：
	- 使用 Bytedesk 服务器实现用户系统、认证、角色/权限与房间策略：https://github.com/Bytedesk/bytedesk
	- 在微语视频会议中配置 Bytedesk API 地址与 Jitsi 服务器 URL，并对齐鉴权与房间策略设置。

说明：本仓库聚焦产品文档；应用代码与完整配置示例可能在相关仓库或后续版本中提供。

## 隐私与安全

- 采用 Jitsi 的安全架构（DTLS‑SRTP、基于 Prosody 的信令）
- 支持房间密码、等候室与主持人权限管控
- 自托管可确保媒体与元数据完全在你掌控之中

更多安全细节参考：https://jitsi.org/security/

## 浏览器与设备支持

- 最新版 Chrome、Edge、Firefox（桌面）
- macOS/iOS 上的 Safari
- Android 现代浏览器

实际兼容性受部署配置与网络环境影响。

## 参与贡献

欢迎提交 Issue 与 PR，一起完善文档与体验。

## 许可证

请参阅本仓库中的 `LICENSE` 文件。

## 路线图

- 常见部署的配置示例
- 主题/品牌定制指引
- 自托管场景的管理与统计指南

## 致谢

基于 Jitsi 开发：https://jitsi.org/

