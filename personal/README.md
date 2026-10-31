# 个人代理规则

普通网址编辑根目录 `PersonalProxy.yaml`。需不同出口的业务编辑本目录对应 YAML，避免影音或 AI 走错出口。所有条目均标注用途或本地来源。

首次将主配置加载到 OpenClash 后，每 600 秒通过 GitHub 策略组更新；以后增删域名无需重启核心，可在面板单独更新规则集。GitHub 缓存可能使更新稍有延迟，更新失败时检查日志。规则遵循主配置从上到下的优先级；不支持按 HTTPS 网址路径区分。

|文件|出口/用途|
|---|---|
|personal/egress_check.yaml|出口 IP / 定位与隐私检测|
|personal/shared_static.yaml|Amazon 共用静态资源|
|personal/bulk_download.yaml|下载与软件分发|
|personal/bulk_media.yaml|大流量视频|
|personal/foreign_news.yaml|海外新闻资讯|
|personal/foreign_work.yaml|协作办公|
|personal/foreign_dev.yaml|开发工具与文档|
|personal/foreign_shop.yaml|海外购物|
|personal/foreign_mail.yaml|海外邮箱|
|personal/cloud_web.yaml|云盘网页与在线文档|
|personal/bahamut_video.yaml|巴哈姆特台湾影音|
|PersonalProxy.yaml|personal_proxy|
|personal/personal_japan_video.yaml|personal_japan_video|
|personal/personal_us_media.yaml|personal_us_media|
|personal/personal_fast.yaml|personal_fast|
|personal/personal_github.yaml|personal_github|
|personal/personal_japan_media.yaml|personal_japan_media|

本次迁移本地内嵌域名集及普通/影音等手写代理域名；局域网、直连例外、DNS 引导与 IP 规则仍留在主配置。远程第三方规则集继续按原地址引用。生产路由器尚未应用本地修改。
