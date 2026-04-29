---
title: Guide for Template - Advanced Customization
published: 2024-02-10
description: "Master the advanced features and customization options of the Twilight template."
cover: ""
coverInContent: false
pinned: false
tags: []
category:
    - Guides:
        - Advanced Customization
draft: false
---

:::note
模板教学说明：这是一篇 Twilight 自带的进阶示例文章，主要用于演示主题配置、Markdown 扩展和卡片组件。实际建站时，你可以把这里的示例替换成自己的教程，或者在不需要时删除。
:::

This guide covers advanced customization options and features available in the Twilight template, from global configurations to specialized Markdown extensions.

中文翻译：本指南介绍 Twilight 模板的进阶能力，包括全局配置项、可视化效果、组件调整，以及 Markdown 扩展能力。


## Global Configuration

中文翻译：全局配置主要通过 `twilight.config.yaml` 完成，涉及站点信息、主题样式、背景和侧边栏组件等。

The `twilight.config.yaml` file is the heart of your blog's configuration. Here are some advanced settings you can tweak:

### Site & Localization

- **Language & Translation**: Enable client-side translation using `site.translate.enable`. You can choose different services and configure auto-detection.

- **Custom Fonts**: Add your own fonts by providing a CSS link or file path under `site.font`.

### Visual Effects

- **Theme Color**: Change the primary color of your blog by adjusting the `site.themeColor.hue` (0-360).

- **Wallpaper Modes**: Choose between `banner`, `fullscreen`, or `none`. You can also enable a `carousel` for multiple wallpapers with the `kenBurns` effect.

- **Waves Effect**: Toggle the animated water ripple effect on the banner using `site.wallpaper.banner.waves.enable`.

- **Particle Effects**: Enable floating particles in the background with `particle.enable`.

### UI 

- **Navbar Transparency**: Adjust `site.wallpaper.banner.navbar.transparentMode` between `semi`, `full`, or `semifull`.

- **Sidebar Widgets**: Reorder or toggle sidebar components like `profile`, `announcement`, `categories`, `tags`, `toc`, and `statistics` in `sidebar.components`.


## Markdown Extensions

中文翻译：这一节演示 Markdown 扩展功能，例如 GitHub 卡片、音乐卡片、提示块（admonitions）和 spoiler 语法。

### GitHub Repository Cards

You can add dynamic cards that link to GitHub repositories, on page load, the repository information is pulled from the GitHub API. 

::github{repo="Spr-Aachen/Twilight"}

Create a GitHub repository card with the code `::github{repo="Spr-Aachen/Twilight"}`.

```markdown
::github{repo="Spr-Aachen/Twilight"}
```

### Music Cards

- Online
::music{meting="https://meting.spr-aachen.com/api?server=netease&type=song&id=1390882521"}

```markdown
::music{meting="https://meting.spr-aachen.com/api?server=netease&type=song&id=1390882521"}
```

- Local
::music{title="深海之息" artist="Youzee Music" cover="https://p1.music.126.net/PhKOqFtljgHDDpKYM2ADUA==/109951169858309716.jpg" audio="assets/music/深海之息.m4a" lrc="assets/music/深海之息.lrc"}

```markdown
::music{title="深海之息" artist="Youzee Music" cover="https://p1.music.126.net/PhKOqFtljgHDDpKYM2ADUA==/109951169858309716.jpg" audio="assets/music/深海之息.m4a" lrc="assets/music/深海之息.lrc"}
```

### Admonitions

Following types of admonitions are supported: `note` `tip` `important` `warning` `caution`

:::note
Highlights information that users should take into account, even when skimming.
:::

:::tip
Optional information to help a user be more successful.
:::

:::important
Crucial information necessary for users to succeed.
:::

:::warning
Critical content demanding immediate user attention due to potential risks.
:::

:::caution
Negative potential consequences of an action.
:::

- **Basic Syntax**

    ```markdown
    :::note
    Highlights information that users should take into account, even when skimming.
    :::

    :::tip
    Optional information to help a user be more successful.
    :::
    ```

- **Custom Titles**

    The title of the admonition can be customized.
    :::note[MY CUSTOM TITLE]
    This is a note with a custom title.
    :::
    ```markdown
    :::note[MY CUSTOM TITLE]
    This is a note with a custom title.
    :::
    ```

- **GitHub Syntax**

    > [!TIP]
    > [The GitHub syntax](https://github.com/orgs/community/discussions/16925) is also supported.
    ```markdown
    > [!TIP]
    > The GitHub syntax is also supported.
    ```

- **Spoiler**

    You can add spoilers to your text. The text also supports **Markdown** syntax.

    The content :spoiler[is hidden **ayyy**]!
    ```markdown
    The content :spoiler[is hidden **ayyy**]!
    ```

---

For more details, check the [Documentation](https://docs.twilight.spr-aachen.com).

中文翻译：更多完整用法请查看官方文档 [Documentation](https://docs.twilight.spr-aachen.com)。