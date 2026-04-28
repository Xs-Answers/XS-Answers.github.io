---
title: Guide for Template - Getting Started
published: 2001-10-02
description: "How to use this blog template."
cover: "./cover.jpg"
coverInContent: false
pinned: true
tags: []
category:
    - Guides:
        - Getting Started
draft: false
---

:::note
模板教学说明：这是一篇 Twilight 自带的入门示例文章，主要用于演示文章 Front-matter 和目录结构。你可以保留它作为参考，也可以在熟悉后改写成自己的内容，或者直接删除。
:::

Tip: For the things that are not mentioned in this guide, you may find the answers in the [Astro Docs](https://docs.astro.build/).

中文翻译：提示，如果本指南没有提到你遇到的问题，可以在 [Astro 文档](https://docs.astro.build/) 中继续查找答案。


## Front-matter of Posts

中文翻译：这一节展示文章头部 Front-matter 的常用字段格式，创建新文章时可直接参考。

```yaml
---
title: My First Blog Post
published: 2020-02-02
description: This is the first post of my new Astro blog.
cover: ./cover.jpg
coverInContent: false
tags: []
category: Guides
comment: true
draft: false
---
```


| Attribute        | Description      |
|------------------|------------------|
| `title`          | The title of the post. |
| `published`      | The date the post was published. |
| `pinned`         | Whether this post is pinned to the top of the post list. |
| `description`    | A short description of the post. Displayed on index page. |
| `cover`          | The cover image path of the post. <br/>1. Start with `http://` or `https://`: For web image <br/>2. Start with `/`: For image in `public` dir <br/>3. With none of the prefixes: Relative to the markdown file |
| `coverInContent` | Whether to show the cover image in the post content. |
| `tags`           | The tags of the post. |
| `category`       | The category of the post <br/>1. Single category: `category: Guides` <br/>2. Multi-category: `category: [Guides, Getting Started]` |
| `licenseName`    | The license name for the post content. |
| `author`         | The author of the post. |
| `sourceLink`     | The source link or reference for the post content. |
| `comment`        | Whether to enable comment for this post. Default is `true`. |
| `draft`          | If this post is still a draft, which won't be displayed. |

中文翻译：上表说明了常见字段的用途，其中 `pinned` 控制是否置顶，`draft` 为 `true` 时文章不会在正式环境显示。


## Where to Place the Post Files

Your post files should be placed in `src/content/posts/` directory. You can also create sub-directories to better organize your posts and assets.

中文翻译：文章文件建议放在 `src/content/posts/` 目录中，也可以按主题建立子目录来整理文章与配图资源。

```
src/content/posts/
├── post-1.md
└── post-2/
    ├── cover.jpg
    └── index.md
```