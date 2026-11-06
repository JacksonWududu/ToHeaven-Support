# ToHeaven Support

ToHeaven 的独立静态支持网站项目，包含使用条款、隐私政策和联系方式。开发者为 **yanhao wu**，支持邮箱为 **BloatMonster@163.com**。

网站正文采用与 App 当前界面一致的英文。全部资源保存在本目录，不需要安装依赖、构建工具、服务器数据库或第三方字体；页面在禁用 JavaScript 时也可完整阅读。

本项目工作区为 `/Users/jackson/Documents/Codex/ToHeaven-Support`，与 App 的 `/Users/jackson/Documents/Codex/ToHeaven` 并列。网站使用自己的 `.git`，不作为 App 仓库的子目录、子模块或 worktree。

## 产品理念

ToHeaven 为那些仍想说、却无法再当面对话的话提供一个书写的地方：写给逝去的亲人，写给想念却无法对话的人，也写给过去的自己。信可以承载回忆、感谢、遗憾或尚未说出口的话；不要求写作者告别、放下或得出一个完整的结局。

后续文案保持温柔、克制，尊重每个人书写的节奏。寄出与燃烧表达的是个人的象征性仪式，不承诺真实投递、与逝者建立联系或特定的情绪改善效果。

## 页面

| 文件 | 用途 |
| --- | --- |
| `index.html` | 支持与法律信息首页 |
| `support.html` | 联系开发者、问题反馈与常见问题 |
| `privacy.html` | 当前功能对应的隐私政策 |
| `terms.html` | 自定义使用条款 |
| `assets/style.css` | 全站共享样式 |
| `assets/app-icon.png` | 复用 App 已确认图标 |

## 本地预览

在本目录执行：

```sh
python3 -m http.server 8765 --bind 127.0.0.1
```

浏览器打开 [本地预览](http://127.0.0.1:8765/)。预览结束后在终端按 Control-C 停止服务器。

## 后续通过 GitHub Pages 发布

本次只准备本地网站，不创建远程仓库、不上传 App 源码、不发布网页。

1. 为本项目的独立本地 Git 仓库配置专用 GitHub 远程仓库；仅上传本网站文件，不上传同级 ToHeaven App 工程。
2. 将网站文件提交到该仓库的 `main` 分支。
3. 仓库 **Settings → Pages → Build and deployment** 中选择 **Deploy from a branch**。
4. 分支选择 **main**，目录选择 **/ (root)**，保存。`.nojekyll` 保证按静态文件发布。
5. 以 GitHub 实际返回的 Pages 地址为准，启用 HTTPS，验证首页及三个子页面都能直接访问。所有站内路径均为相对路径，支持仓库子路径。
6. 将实际站点下的 `privacy.html` 填入 App Store Connect 的 Privacy Policy URL，将 `support.html` 填入 Support URL。`terms.html` 用作 App 内条款入口。
7. 在 App 设置页接入三个已验证的实际地址。当前 `terms.html` 是自行编写的功能使用条款，补充说明 App 行为，App 许可继续适用 Apple 标准 EULA；不要将该网页正文直接当成 App Store Connect 的完整 Custom EULA。若以后要替换 Apple 标准许可，需要补充开发者地址、电话及 Apple 要求的全部最低条款后再单独配置。

发布方式依据 [GitHub Pages 官方文档](https://docs.github.com/en/pages/getting-started-with-github-pages/configuring-a-publishing-source-for-your-github-pages-site)。目前没有仓库用户名、仓库名或域名配置，因此没有编造正式网址。

## 内容维护

- 政策按当前本地保存功能撰写，App 不提供账户、云同步或实际邮寄／消息投递。
- 系统备份、恢复旧备份和支持邮件与 App 主动上传信件是不同的数据处理行为，政策中分别说明。
- 发布前实际验证支持邮箱可收发邮件；代码检查不能证明邮箱可投递。
- 新增联网、分析、广告、账户、订阅或云同步前，先重新核对并更新政策、条款与 App Store 隐私申报。
- GitHub Pages 作为网站托管方可能处理访问者的技术数据；网站不添加分析脚本、广告、表单或 Cookie 代码。
- 修改法律正文时同步更新页面的 Last updated 日期。不要在网页中放置真实信件、用户照片或其他私人测试数据。

本项目与 App 工程独立维护，不依赖 App 工作区中的文件或 Git 历史。
