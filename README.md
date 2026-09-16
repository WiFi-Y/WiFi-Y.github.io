# WanFang Yang 的个人主页

蓝色主题的静态个人主页，提供独立的英文版和中文版，适配电脑与手机。

- [英文首页（默认）](https://wifi-y.github.io/)
- [中文版](https://wifi-y.github.io/zh.html)
- [实验室主页](https://csu-jpg.github.io/#home)

## 文件说明

| 文件 | 用途 |
| --- | --- |
| `index.html` | 默认英文首页 |
| `zh.html` | 中文版，通过右上角按钮切换 |
| `static/css/root.css` | 主题颜色 |
| `static/css/style.css` | 排版与手机布局 |
| `images/avator.jpg` | 个人头像 |
| `images/favicon.svg` | 浏览器标签页的字母图标 |
| `images/research-placeholder.svg` | 英文版研究图片占位 |
| `images/research-placeholder-zh.svg` | 中文版研究图片占位 |

两版共享样式和图片资源，文字分别维护，不会自动翻译。旧模板的其他静态资源目前未被页面引用。

## 更新内容

分别在 `index.html` 和 `zh.html` 中修改对应栏目，英文页填写英文，中文页填写中文。

### 研究方向

第一栏“关于我”用于介绍研究方向与兴趣。找到 `id="about"`，替换 `class="research-interests"` 段落中的占位文字。

### 研究项目与论文

找到 `id="research"`。已有项目和论文两种示例卡片，复制完整的 `<article class="research-card">...</article>` 即可新增条目。

1. 将照片或示意图放进 `images/`。
2. 将卡片中图片的 `src` 替换为图片路径，例如 `images/my-project.jpg`；同时更新 `alt`，简要描述图片。
3. 替换标题、简介、作者及关键词。论文卡片可填写会议或期刊和年份。
4. 需要链接时，在 `research-copy` 内添加下面这样的链接，并换成真实地址：

```html
<a class="research-link" href="https://github.com/WiFi-Y"
   target="_blank" rel="noopener noreferrer">项目链接 ↗</a>
```

英文版请将链接文字改为英文。填写真实内容后，删除不需要的示例卡片和该栏目中的 `template-note` 提示。

### 消息动态

找到 `id="news"`。动态只使用日期和文字，可按需添加链接，不放照片。复制 `news-list` 中的一条 `<li>...</li>` 即可新增通知，建议最新消息放在最前面。

```html
<li>
  <span class="news-date">2026.09</span>
  <p>在这里填写消息内容。
    <a href="https://github.com/WiFi-Y" target="_blank"
       rel="noopener noreferrer">相关链接 ↗</a>
  </p>
</li>
```

没有链接时删除 `<a>...</a>` 即可。英文版请填写英文消息和链接文字。填写真实消息后，删除示例通知及该栏目中的 `template-note` 提示。

### 教育经历与联系方式

- 教育经历单独放在 `id="education"`，位于研究成果和动态之后。
- 左侧个人信息位于 `<aside class="profile">`，包含姓名、在读身份、学校、邮箱、GitHub 和实验室链接。
- 修改邮箱时，同时更新左侧和底部联系区域的邮箱文字及 `mailto:` 地址。

## 本地查看与发布

直接用浏览器打开 `index.html` 即可查看。也可以在项目目录运行：

```bash
python -m http.server 8000 --bind 127.0.0.1
```

然后打开 [本地预览](http://127.0.0.1:8000/)。完成修改后提交并推送到 GitHub；线上站点由仓库的 GitHub Pages 配置发布，可在仓库的 Actions 和 Settings → Pages 中查看发布状态。

## 当前内容

- 姓名：WanFang Yang
- 硕士：中南大学，计算机科学与技术，2026–至今
- 本科：中南大学，软件工程，2022–2026
- 邮箱：264711042@csu.edu.cn
- GitHub：[WiFi-Y](https://github.com/WiFi-Y)

研究方向尚未填写，研究成果和动态目前是用于预览布局的示例模板。
