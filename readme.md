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
- Deployment: [GitHub Pages](https://pages.github.com/) & [Cloudflare Pages](https://pages.cloudflare.com)
- Publish directory: `public`
- Builds: `Active`

## Domains

Use your own domain

### Custom domains

- Default subdomain: [mksalada.github.io](https://mksalada.github.io)
- Primary domain: ~~[tina.codekit.org](https://tina.codekit.org)~~ [tinasalada.pages.dev](https://tinasalada.pages.dev)
- Redirects automatically to primary domain: [mksalada.github.io](https://mksalada.github.io)
- Domain alias: ~~[tina.codekit.org](https://tina.codekit.org)~~ [tinasalada.pages.dev](https://tinasalada.pages.dev)

> **Goal:**
> Subdomain: [mks.is-a.dev](https://mks.is-a.dev)

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

### Update the submodule (theme)

```cmd
git submodule update --remote --merge
```

### Print a module dependency graph (Hugo)

- Run "`hugo mod graph`" for more information

### Create new content inside a folder

```bash
hugo new content sample/external/index.md
```

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

## Folder structures

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

## Page structures

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

# Hugo

```cmd
hugo is the main command, used to build your Hugo site.

Hugo is a Fast and Flexible Static Site Generator
built with love by spf13 and friends in Go.

Complete documentation is available at https://gohugo.io/.   

Usage:
  hugo [flags]
  hugo [command]

Available Commands:
  completion  Generate the autocompletion script for the specified shell
  config      Print the site configuration
  convert     Convert your content to different formats      
  deploy      Deploy your site to a Cloud provider.
  env         Print Hugo version and environment info        
  gen         A collection of several useful generators.     
  help        Help about any command
  import      Import your site from others.
  list        Listing out various types of content
  mod         Various Hugo Modules helpers.
  new         Create new content for your site
  server      A high performance webserver
  version     Print Hugo version and environment info        

Flags:
  -b, --baseURL string             hostname (and path) to the root, e.g. https://spf13.com/
  -D, --buildDrafts                include content marked as 
draft
  -E, --buildExpired               include expired content   
  -F, --buildFuture                include content with publishdate in the future
      --cacheDir string            filesystem path to cache directory
      --cleanDestinationDir        remove files from destination not found in static directories
      --clock string               set the clock used by Hugo, e.g. --clock 2021-11-06T22:30:00.00+09:00
      --config string              config file (default is hugo.yaml|json|toml)
      --configDir string           config dir (default "config")
  -c, --contentDir string          filesystem path to content directory
      --debug                      debug output
  -d, --destination string         filesystem path to write files to
      --disableKinds strings       disable different kind of 
pages (home, RSS etc.)
      --enableGitInfo              add Git revision, date, author, and CODEOWNERS info to the pages
  -e, --environment string         build environment
      --forceSyncStatic            copy all files when static is changed.
      --gc                         enable to run some cleanup tasks (remove unused cache files) after the build
  -h, --help                       help for hugo
      --ignoreCache                ignores the cache directory
      --ignoreVendorPaths string   ignores any _vendor for module paths matching the given Glob pattern
  -l, --layoutDir string           filesystem path to layout 
directory
      --logLevel string            log level (debug|info|warn|error)
      --minify                     minify any supported output format (HTML, XML etc.)
      --noBuildLock                don't create .hugo_build.lock file
      --noChmod                    don't sync permission mode of files
      --noTimes                    don't sync modification time of files
      --panicOnWarning             panic on first WARNING log      --poll string                set this to a poll interval, e.g --poll 700ms, to use a poll based approach to watch for file system changes
      --printI18nWarnings          print missing translations      --printMemoryUsage           print memory usage to screen at intervals
      --printPathWarnings          print warnings on duplicate target paths etc.
      --printUnusedTemplates       print warnings on unused templates.
      --quiet                      build in quiet mode       
      --renderSegments strings     named segments to render (configured in the segments config)
  -M, --renderToMemory             render to memory (mostly useful when running the server)
  -s, --source string              filesystem path to read files relative from
      --templateMetrics            display metrics about template executions
      --templateMetricsHints       calculate some improvement hints when combined with --templateMetrics
  -t, --theme strings              themes to use (located in 
/themes/THEMENAME/)
      --themesDir string           filesystem path to themes 
directory
      --trace file                 write trace to file (not useful in general)
  -v, --verbose                    verbose output
  -w, --watch                      watch filesystem for changes and recreate as needed

Use "hugo [command] --help" for more information about a command.
```
