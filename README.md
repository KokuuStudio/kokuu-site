# KOKUU 谷雨工作室

静态展示站 · [kokuu.org](https://kokuu.org)

一个零依赖的单文件静态网站，用于展示 KOKUU 谷雨工作室的业务与理念。

## 业务

- **Minecraft 服务器运营**（主营，非商业化，用爱发电，一起玩）
- **皮肤站**（站点 + 登录验证服务）
- **AI 变声器**（成品模型交付）

## 技术

- 纯 HTML + 内联 CSS/JS，**零外部依赖**
- Canvas 像素动画（雨滴 + 闯关小人），带统一帧调度与省电模式，兼容老旧设备
- 资源目录：`assets/`（logo 的 PNG/WebP 双格式、favicon）

## 本地预览

直接用浏览器打开 `index.html` 即可；或起一个本地静态服务器：

```bash
python -m http.server 8080
# 然后访问 http://localhost:8080
```

## 线上

- 仓库：<https://github.com/KokuuStudio/kokuu-site>
- 站点（GitHub Pages）：<https://kokuustudio.github.io/kokuu-site/>

## 更新

```bash
git add -A
git commit -m "说明改了什么"
git push
```
