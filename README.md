# kabuda-legal

Kabuda（iOS 相机 App，Bundle `com.kabuda.app`）的**隐私政策**与**用户协议**静态页，托管在 GitHub Pages。

- 隐私政策：`privacy/index.html`
- 用户协议：`terms/index.html`
- 索引页：`index.html`（可选，避免仓库根路径 404）

两个页面都是**中英双语单文件**：按浏览器语言（`navigator.language`）自动显示，顶部按钮可手动切换，
也支持 `?lang=zh` / `?lang=en` 覆盖。App 内中英文指向**同一个 URL**。

## 一、主体信息（已填）

- 中文：**王港锋（GANGFENG WANG）**，个人开发者
- 英文：**GANGFENG WANG**，an individual developer
- 邮箱：`vnues.wgf@gmail.com`

⚠️ 与 Apple 后台（App Store Connect → 用户信息 → Legal Entity Name）**逐字一致**，改之前先回后台核对。

## 一·补、发布前仍需核对的项

1. **生效日期 / 更新日期**（默认写了 `2026-10-06`，实际以提审日为准）。
2. **联系邮箱**（默认 `vnues.wgf@gmail.com`，中英一起改）。
3. 如需要，补充联系地址（各页「联系我们 / Contact us」一节）。

- 仓库：<https://github.com/rokiai/kabuda-legal>
- remote：`git@github.com-rokiai:rokiai/kabuda-legal.git`（本机 `~/.ssh/config` 里 `github.com-rokiai` 这个别名把 rokiai 的钥匙钉死，
  默认的 `github.com` 走的是另一个账号，直接 push 会 `Permission denied`。）

## 二、开 Pages（一次性）

1. 本仓库必须是 **Public**（免费账号的私有仓开不了 Pages ⇒ 审核员打不开 = 当缺失）。
2. GitHub 仓库页 → `Settings` → `Pages` → Source 选 **Deploy from a branch** → Branch `main`、目录 `/ (root)` → Save。
3. 1–2 分钟后页面顶部出现绿色提示，得到：
   - 隐私政策：<https://rokiai.github.io/kabuda-legal/privacy/>
   - 用户协议：<https://rokiai.github.io/kabuda-legal/terms/>

⛔ 不要把 `raw.githubusercontent.com` 或仓库 blob 页面当正式链接（前者是 text/plain，且在大陆访问不稳）。

## 三、App Store Connect 填哪里

| 位置 | 填什么 |
| --- | --- |
| App 信息 → **隐私政策 URL** | `.../kabuda-legal/privacy/` |
| App 信息 → **自定义许可协议（EULA）** | 用本页就**粘贴全文**；否则留空并用 Apple 标准 EULA |
| App Description | 放一条 **Terms of Use（EULA）** 链接 |
| App 内付费墙 | **两个链接都要可点**：隐私政策 + 条款（⛔ 不许指向同一个 URL） |
| App 隐私（营养标签） | 与隐私政策逐条对得上：相册、相机、麦克风、位置；**无**第三方统计/广告 SDK |

Apple 标准 EULA（不想自定义时用）：<https://www.apple.com/legal/internet-services/itunes/dev/stdeula/>

## 四、订阅页（Guideline 3.1.2）必须同时可见

标题 · 时长 · **本地化价格**（渲染 `Product.displayPrice`，别写死）· 自动续费与取消说明 · 隐私政策链接 · 条款链接。

## 五、可选：绑自己的域名

仓库 Settings → Pages → Custom domain 填 `privacy.<你的域名>`，并在域名 DNS 加一条 **CNAME** 指向
`<用户名>.github.io`。HTTPS 由 GitHub 自动签发。
⚠️ 站点托管在境外 ⇒ 不需要 ICP 备案；若改成境内服务器/境内域名面向大陆服务才需要备案。
