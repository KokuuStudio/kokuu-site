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

## 页面结构

| 章节 | 内容 |
| --- | --- |
| 01 / 我们在做什么 | 三项业务贴纸卡 |
| 02 / 怎么开始 | 每项服务三步上手流程 |
| 03 / 常去的地方 | 真实入口链接（皮肤站 / 论坛 / 邮箱） |
| 04 / 我们怎么做 | 「不做 / 只做」宣言 |
| 05 / 谁在做事 | 四个成员 + 一个空位 |
| 06 / 常见问题 | 六条问答（原生 `<details>` 手风琴） |

## 入口

- 官网：<https://kokuu.org>
- 皮肤站：<https://auth.kokuu.org>
- 论坛：<https://chat.kokuu.org>

## 特性

- **零依赖**：纯 HTML + 内联 CSS/JS，无框架、无构建、无外部请求
- **像素美学**：Canvas 像素动画（雨滴 + 闯关小人），统一帧调度与省电模式
- **响应式**：适配移动端到宽屏
- **移动端字体兼容**：标题用实心色而非空心描边（见下方「已知坑」）
- **GitHub Pages 部署**：`CNAME` 绑定 kokuu.org，`.nojekyll` 绕过 Jekyll 处理

## 已知坑（别再踩）

**中文空心描边标题在移动端不可用。** 依次试过三种实现全部失败：
`color: transparent` + `-webkit-text-stroke`（安卓 OEM 内核渲染异常、文字消失）→
8 方向 `text-shadow` 手工描边（中文笔画细，阴影填满字怀，变成加粗实心块）→
`-webkit-text-fill-color` 空心（高分屏上仍发糊发虚）。
**最终方案：标题一律用实心色，靠墨色/雨青的颜色差做层次。** 不要再尝试描边。

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
