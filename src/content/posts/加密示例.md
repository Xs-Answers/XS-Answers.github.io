---
title: Encryption Example
published: 2020-02-02
description: 'Password: 123456'
encrypted: true
pinned: false
password: "123456"
tags: [Encryption]
category: Examples
---

:::note
模板教学说明：这是一篇模板自带的加密文章示例，用来演示 `encrypted` 和 `password` 字段的用法。它适合拿来测试加密流程，但不建议直接用于存放真正敏感的信息。
:::

# Password Protected Post

This is an example of a password-protected post in the Twilight theme. The content below is encrypted using AES and can only be viewed by entering the correct password.

中文翻译：这是 Twilight 主题的加密文章示例。正文会使用 AES 在前端加密，只有输入正确密码后才能查看内容。


## Frontmatter Example

中文翻译：这一节展示启用加密的 Front-matter 写法，核心字段是 `encrypted` 和 `password`。

```yaml
---
title: Encryption Example
published: 2020-02-02
encrypted: true
password: "your-password"
...
---
```

- `encrypted` - Whether encryption is enabled for the post.
- `password` - The password required to unlock the content.

中文翻译：`encrypted` 用于开启或关闭加密，`password` 是读者解锁文章时需要输入的密码。


## Note

:::warning
Do not use this for extremely sensitive information like bank passwords or private keys. The encryption happens on the client side, and the password itself is stored in the post's metadata (though usually not displayed directly).
:::

中文翻译：请勿把它用于存放极度敏感信息（例如银行卡密码或私钥）。该方案是前端加密，密码仍属于文章元数据的一部分，不适合高安全场景。