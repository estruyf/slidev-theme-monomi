# Slidev - MonoMi Theme

[![NPM version](https://img.shields.io/npm/v/slidev-theme-monomi?color=3AB9D4&label=)](https://www.npmjs.com/package/slidev-theme-monomi)

A **mono**chrome-**mi**nimalist theme for [Slidev](https://github.com/slidevjs/slidev).

<!--
  Learn more about how to write a theme:
  https://sli.dev/guide/write-theme.html
--->

<!--
  run `npm run dev` to check out the slides for more details of how to start writing a theme
-->

<!--
  Put some screenshots here to demonstrate your theme

  Live demo: [...]
-->

## Install

Add the following frontmatter to your `slides.md`. Start Slidev then it will prompt you to install the theme automatically.

<pre><code>---
theme: <b>bold</b>
---</code></pre>

Learn more about [how to use a theme](https://sli.dev/themes/use).

## Theme config

### Light mode

```yaml
themeConfig:
  background: "#000"
  color: "#fff"
  title-font-weight: "900"
  
  box-background: "#fff"
  box-foreground: "#000"
  box-font-weight: "900"

  code-background: "#000"
  code-padding: "5px"

  primary: "#f141a8"
```

### Dark mode

```yaml
themeConfig:
  background: "#fff"
  color: "#000"
  title-font-weight: "900"
  
  box-background: "#000"
  box-foreground: "#fff"
  box-font-weight: "900"

  code-background: "#000"
  code-padding: "5px"

  primary: "#f141a8"
```
