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

```yaml
---
theme: monomi
---
```

Learn more about [how to use a theme](https://sli.dev/themes/use).

## Theme config

The theme supports both light and dark mode. Dark mode is the default.

If you want to switch to light mode, add the following configuration:

```yaml
---
theme: monomi
colorSchema: light
---
```

### Bordered headings

You can add borders to headings by adding the `bordered` class to the heading.

```yaml
---
themeConfig:
  bordered: "5px"
---
```