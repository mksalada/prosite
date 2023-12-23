# Site details

    > General information about the site

## Site information

    - Site name: `Tina Salada`
    - Owner: `mks`, `Tina Salada`, `mksalada`
    - Description: `My blog site`
    - Theme: [Blowfish](https://github.com/nunocoracao/blowfish) by [Dillon](https://github.com/nunocoracao) [![GitHub release (latest by date)](https://img.shields.io/github/v/release/nunocoracao/blowfish?style=flat-square)](https://github.com/nunocoracao/blowfish/releases)

## Build & deploy

    > Settings for Continuous Deployment from a Git repository

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

    > Use your own domain

### Custom domains

    - Default subdomain: [mksalada.github.io](https://mksalada.github.io)
    - Primary domain: [tina.codekit.org](https://tina.codekit.org)
    - Redirects automatically to primary domain: [mksalada.github.io](https://mksalada.github.io)
    - Domain alias: [tina.codekit.org](https://tina.codekit.org)

## Website launching offline

    > Go to http://localhost:1313

    > Launch by using the following command:

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

## Build the website

    - When your site is ready to deploy, run the `hugo` command.
    - A *`public`* folder will be generated, containing all static content and assets for your website. It can now be deployed on any web server.

***

### Resources

    - [Blowfish Documentation](https://blowfish.page/docs/)
    - [Hugo Documentation](https://gohugo.io/documentation/)

### Keyboard Shortcuts

    - Visual Studio Code's [Keyboard Shortcuts Reference](https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf)
    - *Open/New Terminal* -> `Ctrl` + `Shift` + <code>`</code> or `Ctrl` + <code>`</code>
    - *Markdown Preview* -> `Ctrl` + `Shift` + `V`
    - *Markdown Preview to the left* -> `Ctrl` + `K` + `V`
