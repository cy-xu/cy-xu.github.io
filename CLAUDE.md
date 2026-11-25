# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是 Chengyuan (CY) Xu 的个人学术网站,托管在 GitHub Pages 上: https://cy-xu.github.io/ (旧域名 cyxu.tv 已于 2025 年放弃,不要再用)。网站展示研究成果、技术转让项目和过往工作经历。

## 网站架构

- **index.html**: 主页面,包含完整的个人简介、研究项目列表和技术转让项目
- **stylesheet.css**: 全站样式表
- **images/**: 所有图片资源,包括项目截图、头像等
- **wordpress_static/**: 静态化的旧博客文章(遗留内容)
- **zealous_restrained_AI/**: CHI 2023 论文的项目页面
- **Chengyuan_CV.pdf**: 最新简历
- **Chengyuan_CY_Xu_PhD_Dissertation.pdf**: 博士论文全文(63 MB)

## 内容更新指南

### 添加新研究项目

在 `index.html` 的 `<section id="research">` 里复制一个 `<article class="pub">`:

```html
<article class="pub" id="project-id">
  <div class="thumb"><img class="framed" src="images/project-image.png" alt="Short description"></div>
  <a class="pub-title" href="project-url">项目标题</a>
  <div class="pub-meta">
    作者列表(自己用 <strong>Chengyuan Xu</strong>)
    <br><span class="venue">会议/期刊名称</span>
    <br><a href="link1">链接1</a> / <a href="link2">链接2</a>
  </div>
  <div class="pub-body">
    <ul><li>项目亮点</li></ul>
    <p>项目描述</p>
  </div>
</article>
```

- 白底截图加 `class="framed"`(细边框),照片/封面不加
- 桌面:左边 160px 缩略图;手机(<640px):88px 缩略图在标题旁边,作者和正文占满宽度

### 添加技术转让项目

在 `<section id="tech-transfer">` 里,每个公司/类别先放一个分组标签,下面是 `.tt-item`(有公开页面就把标题换成 `<a class="tt-title" href="...">`;和上一项同一年就把 `tt-year` 留空):

```html
<div class="tt-group"><span class="tt-group-name">Adobe Firefly</span><span class="tt-group-years">2023–2026</span></div>

<div class="tt-item">
  <div class="tt-year">年份</div>
  <div>
    <div class="tt-title">项目名称</div>
    <ul>
      <li>简要描述</li>
    </ul>
  </div>
</div>
```

Patents 在 "Patents" 分组里,每项一个标题 + 一行 `.patent-meta`(发明人 · 公开号,公开号包在 `<span class="nowrap">` 里)。

## 部署

网站通过 GitHub Pages 自动部署:
- Push 到 `main` 分支后自动更新
- 网址就是 `https://cy-xu.github.io/`,不用 custom domain(repo 里没有 CNAME 文件)
- 不需要构建步骤,纯静态 HTML

## 重要文件

- **index.html**: 包含 Google Analytics 追踪代码 (G-V2BCPR66BZ)
- 邮箱通过 JavaScript 动态生成以防止爬虫抓取
- 项目图片应放在 `images/` 目录,建议宽度 160px
- PDF 文件直接放在根目录

## 样式约定

- Semantic HTML + CSS grid(不用 table 布局),手机断点 640px
- 所有外部链接使用 `<a>` 标签
- 章节标题 `<h2>`,项目标题 `.pub-title` / `.tt-title`
- 正文左对齐(不用 justify,窄屏会拉开字距)
- 主要内容区域最大宽度 800px
