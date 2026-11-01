---
title: "Markdown 写作速查"
date: 2026-11-01T10:00:00+08:00
draft: false
description: "博客里最常用的 Markdown 语法，放在手边随时查阅。"
tags: ["Markdown", "写作"]
categories: ["工具"]
ShowToc: true
TocOpen: true
---

Markdown 的目标是让写作保持简单。下面是最常用的语法。

## 标题

```markdown
# 一级标题
## 二级标题
### 三级标题
```

## 强调与链接

```markdown
**加粗**
*斜体*
[链接文字](https://example.com)
```

效果分别是：**加粗**、*斜体*、[链接文字](https://example.com)。

## 列表

```markdown
- 第一项
- 第二项
  - 子项

1. 第一步
2. 第二步
```

## 引用

```markdown
> 把复杂的事情写清楚，本身就是一种思考。
```

> 把复杂的事情写清楚，本身就是一种思考。

## 代码

行内代码使用反引号：`hugo server -D`。

代码块可以指定语言，Hugo 会自动做语法高亮：

```yaml
title: "ming"
theme: "PaperMod"
```

## 表格

| 项目 | 用途 |
| --- | --- |
| `content/posts` | 存放文章 |
| `static/images` | 存放图片 |
| `hugo.yaml` | 站点配置 |

## 图片

把图片放到 `static/images/`，然后在文章里引用：

```markdown
![图片说明](/images/example.jpg)
```

图片路径以 `/` 开头，表示从站点根目录开始。
