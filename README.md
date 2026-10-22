# Xiping Sun — personal website

这是一个无需构建、没有第三方依赖的纯静态网站。上传时请使用**本文件夹里的内容**，不要把文件夹本身再嵌套一层。根目录必须能看到 `index.html`。

## 上传到 GitHub

1. 打开 `XipingSun/XipingSun.github.io` 仓库，在上传前备份旧网站。
2. 用本文件夹的内容替换旧网站文件；不要与旧模板混合。保留隐藏文件 `.nojekyll`，让 GitHub Pages 直接发布 HTML。
3. 在仓库 **Settings → Pages → Build and deployment** 中选择 **Deploy from a branch**，选择你上传的分支及 **/ (root)**，然后保存。
4. 发布完成后访问 https://XipingSun.github.io/ 。如果原仓库用了 Jekyll 专用的 Actions 部署工作流，请改用上述 branch 发布方式。

## 文件结构

```text
index.html                 首页：介绍、Research interests、News、研究卡片
publications/index.html    Publications
assets/docs/CV.pdf         你的原始 PDF 简历
cv-json/index.html         旧 CV 地址跳转到 PDF
fun/index.html             Riley 的照片与介绍
assets/css/style.css       所有样式及手机适配
images/                    网站实际用到的 7 个图片/图标文件
.nojekyll                  GitHub Pages 直接发布静态文件
```

## 修改内容

- 更新 News：编辑 `index.html` 中的 `academic-news` 区块；每条消息是一个 `news-item`。
- 更新研究项目：编辑首页和 Publications 页的 `research-card` 区块。复制一张卡片即可增加项目，图片放在 `images/` 中。
- 更换头像：替换 `images/xiping.png`。
- 更换 CV：替换 `assets/docs/CV.pdf`。首页的 CV 按钮会直接打开该 PDF，旧 `/cv-json/` 地址也会自动跳转。
- 修改颜色与间距：编辑 `assets/css/style.css`。

可直接双击 `index.html` 预览，也可以在此文件夹运行 `python3 -m http.server 8000`，然后访问 http://localhost:8000 。

研究信息沿用原网站，并参照 https://chen-yanjun.com/ 补全 NailBender 与 Strain2Force 的作者、会议及获奖信息；这两个项目的缩略图也来自该共同作者站点。未加入旧模板中的示例论文、示例 CV、默认博客或其他未使用的图片。

## 侧栏图标来源

复用了旧站的图标轮廓，内嵌 SVG，无需下载字体或外部服务：Font Awesome Free 6.5.2（Fonticons，https://fontawesome.com/license/free ，CC BY 4.0 / SIL OFL 1.1）与 Academicons 1.9.4（James Walsh、Katja Bercic，https://jpswalsh.github.io/academicons/ ，SIL OFL 1.1）。

导航栏提供 Home / Publications / Fun；CV 位于首页头像侧栏的联系方式下方，作为独立 PDF 按钮。News 默认显示最近三条消息，点击 Earlier updates 可展开较早的两条消息；悬停或键盘聚焦时会突出对应条目。

视觉配色使用深青绿主色、浅鼠尾草绿 News 面板，以及四种柔和底色的研究兴趣标签。News 中的 Read more 链接已移除，较早的 ICRA 项目网站链接保留。
