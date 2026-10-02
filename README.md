# KOKUU 谷雨工作室 · 官网

> 雨落下之后，就交给时间。

静态展示站 · **<https://kokuu.org>**

零依赖的单文件静态网站，用于展示 KOKUU 谷雨工作室的业务与理念。

## 业务

| | |
| --- | --- |
| 🎮 **Minecraft 服务器** | 运营与维护，非商业化，用爱发电，一起玩 |
| 🧩 **皮肤站** | 站点 + 登录验证服务（[KokuuSkin](https://github.com/KokuuStudio/kokuu-home)） |
| 🎨 **AI 变声器** | 成品模型交付 |

## 特性

- **零依赖**：纯 HTML + 内联 CSS/JS，无框架、无构建、无外部请求
- **像素美学**：Canvas 像素动画（雨滴 + 闯关小人），统一帧调度与省电模式
- **响应式**：适配移动端到宽屏
- **GitHub Pages 部署**：`CNAME` 绑定 kokuu.org，`.nojekyll` 绕过 Jekyll 处理

## 目录

```
kokuu-site/
├── index.html               # 单文件站点（结构 + 样式 + 动画全内联）
├── CNAME                    # 自定义域名绑定
├── .nojekyll                # 禁用 Jekyll 处理
└── assets/
    ├── KOKUU-logo-ink.png   # logo 位图
    ├── KOKUU-logo-ink.webp  # logo 现代格式
    └── favicon.png          # 站点图标
```

## 本地预览

直接用浏览器打开 `index.html` 即可；或起一个本地静态服务器：

```bash
python -m http.server 8080
# 然后访问 http://localhost:8080
```

## 更新

```bash
git add -A
git commit -m "说明改了什么"
git push
```

推送到 `main` 分支后 GitHub Pages 会自动重新部署。

## 相关项目

- 皮肤站插件套件：[kokuu-home](https://github.com/KokuuStudio/kokuu-home) ·
  [kokuu-ui](https://github.com/KokuuStudio/kokuu-ui) ·
  [kokuu-quote](https://github.com/KokuuStudio/kokuu-quote)

## 许可

代码以 [MIT](LICENSE) 发布。
「Minecraft」相关商标与素材归各自权利人所有，本项目与之无关联。
