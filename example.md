---
theme: ./

# themeConfig:
#   background: "#fff"
#   color: "#000"
#   title-font-weight: "900"
  
#   box-background: "#000"
#   box-foreground: "#fff"
#   box-font-weight: "900"

#   code-background: "#000"
#   code-padding: "5px"

#   primary: "#f141a8"
---

# Slidev - MonoMi Theme

&mdash; by Elio Struyf

---
layout: about-me

position: left # left, right - Default: right
helloMsg: Hello!
name: Elio Struyf
imageSrc: https://elio.dev/eliostruyf_bw_cutout.png
# imageSrc: https://elio.dev/eliostruyf_bw_black_cutout.png
job: Struyf Consulting
line1: "#Stickerpreneur @ pyod.shop"
line2: "#Maintainer @ Front Matter CMS"
social1: "@eliostruyf"
social2: eliostruyf.com
social3: elio@struyfconsulting.be
---

---

# What is Slidev?

Slidev is a slide maker and presentation tool designed for developers. It includes the following features:

- 📝 **Text-based** - focus on your content with Markdown, then style it later
- 🎨 **Themable** - themes can be shared and reused as npm packages
- 🧑‍💻 **Developer Friendly** - code highlighting, live coding with autocompletion
- 🤹 **Interactive** - embed Vue components to enhance your expressions
- 🎥 **Recording** - built-in recording and camera view
- 📤 **Portable** - export to PDF, PPTX, PNGs, or even a hostable SPA
- 🛠 **Hackable** - virtually anything that's possible on a webpage is possible in Slidev

<br>
<br>

Read more about [Why Slidev?](https://sli.dev/guide/why)

---

# Navigation

Hover on the bottom-left corner to see the navigation's controls panel

## Keyboard Shortcuts

|     |     |
| --- | --- |
| <kbd>space</kbd> / <kbd>tab</kbd> / <kbd>right</kbd> | next animation or slide |
| <kbd>left</kbd>  / <kbd>shift</kbd><kbd>space</kbd> | previous animation or slide |
| <kbd>up</kbd> | previous slide |
| <kbd>down</kbd> | next slide |

---
layout: image-right
image: https://cover.sli.dev
---

# Code

Use code snippets and get the highlighting directly!

```ts
interface User {
  id: number
  firstName: string
  lastName: string
  role: string
}

function updateUser(
  id: number, 
  update: Partial<User>
) {
  const user = getUser(id)
  const newUser = { ...user, ...update }
  saveUser(id, newUser)
}
```

---
layout: center
class: "text-center"
---

# Learn More

[Documentation](https://sli.dev) / [GitHub Repo](https://github.com/slidevjs/slidev)
