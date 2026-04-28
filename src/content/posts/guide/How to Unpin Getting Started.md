---
title: 如何取消 Guide for Template - Getting Started 的置顶
published: 2026-04-28
description: "说明如何取消 Twilight 模板内置 Getting Started 文章的置顶状态。"
coverInContent: false
pinned: false
tags: [Twilight, Guide]
category:
    - Guides:
        - Getting Started
draft: false
---

:::note
这篇文章专门说明如何取消模板示例文章 Guide for Template - Getting Started 的置顶，不会自动修改原文章内容。
:::

## 置顶是由哪个字段控制的

Twilight 的文章列表会优先显示 `pinned: true` 的文章。

目前模板里的 Getting Started 文章位于 [src/content/posts/guide/Getting Started.md](src/content/posts/guide/Getting Started.md)，它的 Front-matter 里有这一行：

```yaml
pinned: true
```

只要这个值是 `true`，这篇文章就会排在文章列表顶部。

## 如何取消置顶

打开 [src/content/posts/guide/Getting Started.md](src/content/posts/guide/Getting Started.md)，把这一行：

```yaml
pinned: true
```

改成：

```yaml
pinned: false
```

保存后重新构建或重新部署站点，文章列表就会恢复为按发布时间排序，这篇文章也不会再显示置顶图标。

## 为什么这样改就生效

文章排序逻辑会先判断 `pinned`，再判断发布时间。也就是说：

1. `pinned: true` 的文章会优先排在前面。
2. 当多篇文章都不是置顶时，才会继续按发布时间从新到旧排序。

## 如果你还想彻底移除这篇模板文章

除了取消置顶，你也可以直接：

1. 修改这篇文章的标题和正文，改成你自己的内容。
2. 或者直接删除 [src/content/posts/guide/Getting Started.md](src/content/posts/guide/Getting Started.md)。

这样首页就不会再显示模板默认教程。