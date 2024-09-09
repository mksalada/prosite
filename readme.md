# Site details

 General information about the site

## Site information

- Site name: `Tina Salada`
- Owner: `mks`, `Tina Salada`, `mksalada`
- Description: `My awesome website`
- Theme: [Blowfish](https://github.com/nunocoracao/blowfish) by [Nuno Coração](https://github.com/nunocoracao)
[![GitHub release (latest by date)](https://img.shields.io/github/v/release/nunocoracao/blowfish?style=flat-square)](https://github.com/nunocoracao/blowfish/releases)

## Build & deploy

Settings for Continuous Deployment from a Git repository

### Repository

- Current repository: [github.com/mksalada/mksalada.github.io](https://github.com/mksalada/mksalada.github.io/)

### Build settings

- Base directory: `main`
- Build command: `hugo`
[![Hugo](https://img.shields.io/badge/Hugo-%5E0.101.0-ff4088?style=flat-square&logo=hugo)](https://gohugo.io/)
- Hosted: [GitHub](https://github.com/)
- Deployment: [GitHub Pages](https://pages.github.com/)
- Publish directory: `public`
- Builds: `Active`

## Domains

Use your own domain

### Custom domains

- Default subdomain: [mksalada.github.io](https://mksalada.github.io)
- Primary domain: [tina.codekit.org](https://tina.codekit.org)
- Redirects automatically to primary domain: [mksalada.github.io](https://mksalada.github.io)
- Domain alias: [tina.codekit.org](https://tina.codekit.org)

## Website launching offline

Go to http://localhost:1313

### Launch by using the following command:

- `hugo serve` or `hugo server`
    + When you run `hugo serve`, when the contents of the files change, the page automatically refreshes with the changes.
- `hugo serve -D` or `hugo serve --buildDrafts`
    + By default all posts and pages are created as a draft. If you want to render these pages, remove the property `draft: true` from the metadata, set the property `draft: false` or add `-D`/`--buildDrafts` parameter to `hugo` command.
- `hugo serve --disableFastRender`
    + Since the theme use ***`.Scratch`*** in Hugo to implement some features, it is highly recommended that you add `--disableFastRender` parameter to hugo server command for the live preview of the page you are editing.
- `hugo serve -e production`
    + Default environments are `development` with `hugo serve` and production with hugo.
    + Due to limitations in the local `development` environment, the **comment system**, **CDN** and **fingerprint** will not be enabled in the `development` environment.
    + You could enable these features with `hugo serve -e production`.
- `hugo serve --cleanDestinationDir`
    + Remove files from destination not found in static directories

### Build the website

- When your site is ready to deploy, run the `hugo` command.
- A *`public`* folder will be generated, containing all static content and assets for your website. It can now be deployed on any web server.

#### Commands

- New Post: `hugo new content posts/new-post-title/index.md`
- New Page: `hugo new content new-page-title/_index.md`
- Start Hugo server: `hugo server --cleanDestinationDir -D`
- Update Blowfish theme through GitHub submodule: `git submodule update --remote --merge`

***

### Resources

- [Blowfish Documentation](https://blowfish.page/docs/)
- [Hugo Documentation](https://gohugo.io/documentation/)

## Keyboard Shortcuts

- Visual Studio Code's [Keyboard Shortcuts Reference](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)
- *Open/New Terminal* -> `Ctrl` + `Shift` + <code>`</code> or `Ctrl` + <code>`</code>
- *Markdown Preview* -> `Ctrl` + `Shift` + `V`
- *Markdown Preview to the left* -> `Ctrl` + `K` + `V`

## Structures

```
.
└── content
    └── projects
        ├── _index.md          # /projects
        ├── first-project.md   # /projects/first-project
        └── another-project
            ├── index.md       # /projects/another-project
            └── project.jpg
```

```md
# /projects/_index.md
---
title: "Projects"
description: "Learn about some of my projects."
cascade:
    showReadingTime: false
    showEdit: false
    showSummary: false
    hideFeatureImage: true
---
This section contains all my current projects.

{{< lead >}}
Blowfish brings your content to life. :heart_eyes:
{{< /lead >}}
```

```md
# /sample/emoji/index.md
---
title: "Emoji :parachute:"
date: 2019-03-05
description: "Guide to Emoji usage in Blowfish"
summary: "📖🏞️🧗🏽🐉🧙🏽‍♂️🧚🏽👸"
tags: ["emoji", "sample"]
type: 'sample'
---

Emoji is supported throughout Blowfish by default. Emoji can be used in titles, menu items and article content.

{{< alert >}}
**Note:** The rendering of these glyphs depends on the browser and the platform. To style the emoji you can either use a third party emoji font or a font stack.
{{< /alert >}}
```

```md
# /sample/external/index.md
---
title: "An External Article"
date: 2019-01-24
externalUrl: "https://nunocoracao.com/projects/"
summary: "The `externalUrl` front matter parameter can link to any URL."
showReadingTime: true
_build:
    render: "false"
    list: "local"
type: 'sample'
---

This page uses the `externalUrl` front matter parameter to link to an article outside of this Hugo website.

It's great for things like linking to posts on Medium or to research papers you may have hosted on third party websites.
```

```txt
https://mks.hashnode.dev/doing-next

Things that I will be doing next
Just discussing my next steps in blogging

Mar 8, 2023

Hello 👋 It's been a very long time since I first published a blog here and many things changed on Hashnode. In my very [first post](https://mks.hashnode.dev/readme), I said that...

> I am only here to read articles of other developers and react & comment to their posts when I'd like to.

I am very consistent with that until now. I will be straight to the point and will not make this long.

I've decided that I will make this my Developer blog site. I will be posting here the story behind my projects as a developer. Not tutorials but stories about how I came up with a project, and so on.

Hope that you guys can also appreciate that!
```

```txt
https://mks.hashnode.dev/readme

What am I doing here?

Jan 27, 2021

> What am I doing here at Hashnode? Why am I not publishing any blog?

That's what always runs through my mind whenever I go here. It's been more than three months since I discovered Hashnode and almost everyone here is encouraging one another to start a blog.

> Can't I just read articles and not write one?

That's the reason I write this post, turn off the comments, hide from the community and clicked publish.

I am only here to read articles of other developers and react & comment to their posts when I'd like to. In that way, I am also learning new stuff and connecting to the community. I believe that Hashnode is not only for developers who write articles but also for those who just read like me. But I want to clarify that I do not forbid myself if ever I want to do blogging here in the future and I do not hate anyone. I honestly love Hashnode's community.

P.S. Right now, I only write personal blogs on my main [website](https://tinasalada.tk/). 😊
```

```txt
Written by
Tina Salada
I believe that Hashnode is not only for developers who write articles but also for those who just read like me.

------

https://mks.hashnode.dev/archive

Archive (3)

Project Blog #1: Temperature Converter Web App
Mar 9, 2023

Things that I will be doing next
Mar 8, 2023

What am I doing here?
Jan 27, 2021
```

```bash
hugo new content projects/temperature-converter/index.md
```

## TODOs
Import blogs at:
- [x] Webnode
- [x] DEV (dev.to)
- [ ] Hashnode
- [ ] WordPress
- [ ] Blogger (blogspot.com)
- [ ] Medium
- [ ] Replit (repl.it)
- [ ] Tumblr
