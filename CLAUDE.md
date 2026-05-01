# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## 项目概述

这是 Chengyuan (CY) Xu 的个人学术网站,托管在 GitHub Pages 上(cyxu.tv)。网站展示研究成果、技术转让项目和过往工作经历。

## 网站架构

- **index.html**: 主页面,包含完整的个人简介、研究项目列表和技术转让项目
- **stylesheet.css**: 全站样式表
- **images/**: 所有图片资源,包括项目截图、头像等
- **wordpress_static/**: 静态化的旧博客文章(遗留内容)
- **zealous_restrained_AI/**: CHI 2023 论文的项目页面
- **Chengyuan_CV.pdf**: 最新简历
- **Chengyuan_CY_Xu_PhD_Dissertation.pdf**: 博士论文全文(63 MB)
- **@CNAME**: 包含自定义域名 `cyxu.tv`

## 内容更新指南

### 添加新研究项目

在 `index.html` 的研究部分(id="Research")添加新的表格行:

```html
<tr id="project-id">
  <td style="padding:20px;width:25%;vertical-align:top">
    <div class="one">
      <img src='images/project-image.png' width="160" style="border: 1px solid grey">
    </div>
  </td>
  <td style="padding:20px;width:75%;vertical-align:middle">
    <a href="project-url">
      <papertitle>项目标题</papertitle>
    </a>
    <br>
    作者列表
    <br>
    <em>会议/期刊名称</em>
    <br>
    <a href="link1">链接1</a> / <a href="link2">链接2</a>
    <ul>
      <li>项目亮点</li>
    </ul>
    <p>项目描述</p>
  </td>
</tr>
```

### 添加技术转让项目

在"Tech Transfer"部分添加新行,格式保持简洁:

```html
<tr>
  <td style="padding-left:20px;width:100%;vertical-align:top">
    <a href="product-link">
      <papertitle>年份 - 项目名称</papertitle>
    </a>
    <br>
    &#8226; 简要描述
  </td>
</tr>
```

## 部署

网站通过 GitHub Pages 自动部署:
- Push 到 `main` 分支后自动更新
- 使用自定义域名 `cyxu.tv` (通过 @CNAME 文件配置)
- 不需要构建步骤,纯静态 HTML

## 重要文件

- **index.html**: 包含 Google Analytics 追踪代码 (G-V2BCPR66BZ)
- 邮箱通过 JavaScript 动态生成以防止爬虫抓取
- 项目图片应放在 `images/` 目录,建议宽度 160px
- PDF 文件直接放在根目录

## 样式约定

- 使用表格布局实现响应式设计
- 所有外部链接使用 `<a>` 标签
- 项目标题使用 `<papertitle>` 标签
- 章节标题使用 `<heading>` 标签
- 主要内容区域最大宽度 800px
