---
title: "开始写第一篇文章"
date: 2026-11-01T09:00:00+08:00
draft: false
description: "这是博客的第一篇文章，也是一份简单的使用说明。"
tags: ["开始", "博客"]
categories: ["随笔"]
ShowToc: true
TocOpen: false
---

欢迎来到这个博客。

这个站点使用 **Hugo** 生成，主题是 **PaperMod**，由 GitHub Actions 自动构建并发布到 GitHub Pages。你只需要写 Markdown，然后把改动推送到 GitHub。

## 写一篇新文章

在项目根目录运行：

```bash
hugo new content posts/my-new-post.md
```

打开生成的文件，把 `draft: true` 改成 `draft: false`，然后开始写正文。

## 本地预览

```bash
hugo server -D
```

浏览器打开 `http://localhost:1313`。

## 发布

```bash
git add .
git commit -m "post: my new post"
git push
```

推送后，GitHub Actions 会自动构建并部署。通常等待一到两分钟，就能在线上看到新文章。

> 写作不需要复杂的后台。一个 Markdown 文件，就是一篇博客。
