# 组织根站点部署包（待管理员部署）

用途：为 https://dart-lab-research.github.io/ 提供可抓取的根首页、favicon 和 WebSite 站点名称说明。当前是部署草稿，并未创建或发布组织仓库。

1. 由组织管理员确认展示名称 `DART Lab Research` 和LLM 字母顶面、受访者与模拟人的立方体图标（目前用于 LLM-S3 项目）可用于整个组织。它们会影响此域名下所有项目的搜索站点标识。
2. 创建公开仓库 `dart-lab-research/dart-lab-research.github.io`。若已存在但当前协作者无权访问，应先检查其内容，不覆盖。
3. 将本目录文件放在仓库根目录，提交至 main。
4. Settings → Pages → Deploy from a branch → main / (root) → Save。
5. 检查根首页、/favicon-96.png 都返回 200。
6. 在 Search Console 添加并验证根 URL 前缀资源 https://dart-lab-research.github.io/，使用该账号提供的验证文件/标签，再请求根首页抓取。原项目路径资源不覆盖根首页。
7. 等待 Google 重新抓取；站点名和图标的采用并不保证，也没有固定生效时间。

项目网址保持原样，本包不会替换项目仓库内容。不需要另买域名。

参考：https://developers.google.com/search/docs/appearance/favicon-in-search
参考：https://developers.google.com/search/docs/appearance/site-names
