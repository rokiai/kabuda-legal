# kabuda-legal

Kabuda（iOS 相机 App）的**隐私政策**与**用户协议**静态页，托管在 GitHub Pages。

- 隐私政策：<https://rokiai.github.io/kabuda-legal/privacy/>
- 用户协议：<https://rokiai.github.io/kabuda-legal/terms/>

两页都是**中英双语单文件**：按浏览器语言（`navigator.language`）自动渲染对应语言，无切换控件；
需要指定时用 `?lang=zh` / `?lang=en`。
App 内中英文指向同一个 URL。

## 本地预览

```bash
python3 -m http.server 8000
# http://localhost:8000/privacy/
```

