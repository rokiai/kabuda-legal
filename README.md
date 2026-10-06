# kabuda-legal

Kabuda（iOS 相机 App）的**隐私政策**与**用户协议**静态页，托管在 GitHub Pages。

- 隐私政策：<https://rokiai.github.io/kabuda-legal/privacy/>
- 用户协议：<https://rokiai.github.io/kabuda-legal/terms/>

两页都是**中英双语单文件**：按浏览器语言自动切换，顶部按钮可手动切，`?lang=zh` / `?lang=en` 可强制指定。
App 内中英文指向同一个 URL。

## 本地预览

```bash
python3 -m http.server 8000
# http://localhost:8000/privacy/
```

## 发布

`git push origin main` —— Pages 自动重新部署，1–2 分钟生效。

## 注意

- 仓库必须 **Public**（免费账号的私有仓开不了 Pages，审核员打不开 = 当缺失）。
- ⛔ 不要用 `raw.githubusercontent.com` 或仓库 blob 页当正式链接（text/plain，且大陆访问不稳）。
- ⛔ 隐私政策 URL 与 EULA（条款）URL **不得指向同一个地址**。
- 页面里的运营主体与联系邮箱是合规必需项，改动前先与 App Store Connect 后台的 legal entity 核对。
- 本机 remote 用 `github.com-rokiai` 这个 SSH 别名；默认的 `github.com` 走另一个账号，直接 push 会被拒。
