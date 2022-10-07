# repo-projects-images-blog-docusaurus

# 🚀 Search repos with a classic docs and blog site built using Docusaurus 2 🚀

https://repo-projects-images-blog-docusaurus.pages.dev

https://github.com/coding-to-music/repo-projects-images-blog-docusaurus

https://repo-projects-images-blog-docusaurus.vercel.app

From / By https://github.com/priambudiLB/priambudiLB

https://fyi-seven.vercel.app

<p align="center"><a href="https://priambudi.fyi"><img width="80px" src="static/img/logo.svg" /></a></p>

<h2>FrontEnd enthusiast. Love to learn, share, and create.</h2>

**About me**

- 💼 [Fulltime] Software Engineer-Web Platform at [Tokopedia](https://www.tokopedia.com/)

- 💼 [Part-time] Fullstack Web Facilitator at [Dibimbing](https://dibimbing.id/)

## Environment variables:

```java

```

## GitHub

```java
git init
git add .
git remote remove origin
git commit -m "first commit"
git branch -M main
git remote add origin git@github.com:coding-to-music/repo-projects-images-blog-docusaurus.git
git push -u origin main
```

## Build message after upgrading to Docusaurus 2.1.0

```
[INFO] [en] Creating an optimized production build...
[ERROR] Unable to build website for locale en.
[ERROR] Error: The "gtag" field in themeConfig should now be specified as option for plugin-google-gtag. For preset-classic, simply move themeConfig.gtag to preset options. More information at https://github.com/facebook/docusaurus/pull/5832.
    at preset (/mnt/volume_nyc1_01/repo-projects-images-blog-docusaurus/node_modules/@docusaurus/preset-classic/lib/index.js:27:15)
```

# Deploying Docusaurus to Cloudflare Pages

https://dev.to/gaurishhs/deploying-docusaurus-to-cloudflare-pages-565g

Docusaurus is a commonly used static site generator. It is built on top of react and can be used to make any kind of site (personal website, product, blog, marketing landing pages, etc).

Cloudflare Pages is a JAMstack platform for frontend developers to collaborate and deploy websites.

## Creating the App

Open up your shiny terminals and create a docusaurus app How to create: https://docusaurus.io/docs/installation#scaffold-project-website

### Creating Docusaurus App

Now, Once you've created change your directory to the project.

Then, Run the start command.

It will open up your browser to the development website: http://localhost:3000/

<img src="images/classic-docusaurus-site.png" alt="classic-docusaurus-site" />

Now, Your Docusaurus Website is ready, Let's deploy it over cloudflare pages.

Change your docusaurus.config.js url field to https://.pages.dev or your custom domain.

Unlike Vercel and netlify, Cloudflare pages doesn't support cli deployments yet (They might come sooner or later)

So, You'll need to push all the code over github.

```
git init
git add -A
git commit -m "initial commit"
git branch -M main
git remote add origin https://github.com/apidev234/Docusaurus-Cf-Pages.git
git push -u origin main
```

After Running these commands, If you check your github, You'll find the code there.

Head to your cloudflare pages dashboard, Signup for pages if you haven't yet.

Create an app and select your github repository.

Choose Create React App as your framework preset.

Create an environment variable NODE_VERSION with the value 16.13.2

Docusaurus requires a node version more than or equal to node v14, 16.13.2 is a LTS(Long time support) Version of Node.js

Then Click Deploy, Within 5mins your app would be ready :)

https://docusaurus-cf-pages.pages.dev/

Add a Custom Domain To Your App https://developers.cloudflare.com/pages/get-started#adding-a-custom-domain

Redirecting www to apex domain https://developers.cloudflare.com/pages/how-to/www-redirect

# Website

This website is built using [Docusaurus 2](https://docusaurus.io/), a modern static website generator.

### Installation

```
$ yarn
```

### Local Development

```
$ yarn start
```

This command starts a local development server and opens up a browser window. Most changes are reflected live without having to restart the server.

### Build

```
$ yarn build
```

This command generates static content into the `build` directory and can be served using any static contents hosting service.

### Deployment

Using SSH:

```
$ USE_SSH=true yarn deploy
```

Not using SSH:

```
$ GIT_USER=<Your GitHub username> yarn deploy
```

If you are using GitHub pages for hosting, this command is a convenient way to build the website and push to the `gh-pages` branch.

---

## description: How to install Docusaurus locally, and start a Docusaurus site in no time.

# Installation

https://docusaurus.io/docs/installation#scaffold-project-website

```mdx-code-block
import Tabs from '@theme/Tabs';
import TabItem from '@theme/TabItem';
```

Docusaurus is essentially a set of npm [packages](https://github.com/facebook/docusaurus/tree/main/packages).

:::tip

Use the **[Fast Track](introduction.md#fast-track)** to understand Docusaurus in **5 minutes ⏱**!

Use **[docusaurus.new](https://docusaurus.new)** to test Docusaurus immediately in your browser!

:::

## Requirements {#requirements}

- [Node.js](https://nodejs.org/en/download/) version 16.14 or above (which can be checked by running `node -v`). You can use [nvm](https://github.com/nvm-sh/nvm) for managing multiple Node versions on a single machine installed.
  - When installing Node.js, you are recommended to check all checkboxes related to dependencies.

## Scaffold project website {#scaffold-project-website}

The easiest way to install Docusaurus is to use the command line tool that helps you scaffold a skeleton Docusaurus website. You can run this command anywhere in a new empty repository or within an existing repository, it will create a new directory containing the scaffolded files.

```bash
npx create-docusaurus@latest my-website classic
```

We recommend the `classic` template so that you can get started quickly, and it contains features found in Docusaurus 1. The `classic` template contains `@docusaurus/preset-classic` which includes standard documentation, a blog, custom pages, and a CSS framework (with dark mode support). You can get up and running extremely quickly with the classic template and customize things later on when you have gained more familiarity with Docusaurus.

You can also use the template's TypeScript variant by passing the `--typescript` flag. See [TypeScript support](./typescript-support.md) for more information.

```bash
npx create-docusaurus@latest my-website classic --typescript
```

:::info FB-Only

If you are setting up a new Docusaurus website for a Facebook open source project, use the `facebook` template instead, which comes with some useful Facebook-specific defaults:

```bash
npx create-docusaurus@latest my-website facebook
```

:::

<details>
  <summary>Alternative installation commands</summary>

You can also initialize a new project using your preferred project manager:

```mdx-code-block
<Tabs>
<TabItem value="npm">
```

```bash
npm init docusaurus
```

```mdx-code-block
</TabItem>
<TabItem value="yarn">
```

```bash
yarn create docusaurus
```

```mdx-code-block
</TabItem>
<TabItem value="pnpm">
```

```bash
pnpm create docusaurus
```

```mdx-code-block
</TabItem>
</Tabs>
```

</details>

Run `npx create-docusaurus@latest --help`, or check out its [API docs](./api/misc/create-docusaurus.md) for more information about all available flags.

## Project structure {#project-structure}

Assuming you chose the classic template and named your site `my-website`, you will see the following files generated under a new directory `my-website/`:

```bash
my-website
├── blog
│   ├── 2019-05-28-hola.md
│   ├── 2019-05-29-hello-world.md
│   └── 2020-05-30-welcome.md
├── docs
│   ├── doc1.md
│   ├── doc2.md
│   ├── doc3.md
│   └── mdx.md
├── src
│   ├── css
│   │   └── custom.css
│   └── pages
│       ├── styles.module.css
│       └── index.js
├── static
│   └── img
├── docusaurus.config.js
├── package.json
├── README.md
├── sidebars.js
└── yarn.lock
```

### Project structure rundown {#project-structure-rundown}

- `/blog/` - Contains the blog Markdown files. You can delete the directory if you've disabled the blog plugin, or you can change its name after setting the `path` option. More details can be found in the [blog guide](blog.mdx)
- `/docs/` - Contains the Markdown files for the docs. Customize the order of the docs sidebar in `sidebars.js`. You can delete the directory if you've disabled the docs plugin, or you can change its name after setting the `path` option. More details can be found in the [docs guide](./guides/docs/docs-introduction.md)
- `/src/` - Non-documentation files like pages or custom React components. You don't have to strictly put your non-documentation files here, but putting them under a centralized directory makes it easier to specify in case you need to do some sort of linting/processing
  - `/src/pages` - Any JSX/TSX/MDX file within this directory will be converted into a website page. More details can be found in the [pages guide](guides/creating-pages.md)
- `/static/` - Static directory. Any contents inside here will be copied into the root of the final `build` directory
- `/docusaurus.config.js` - A config file containing the site configuration. This is the equivalent of `siteConfig.js` in Docusaurus v1
- `/package.json` - A Docusaurus website is a React app. You can install and use any npm packages you like in them
- `/sidebars.js` - Used by the documentation to specify the order of documents in the sidebar

### Monorepos {#monorepos}

If you are using Docusaurus for documentation of an existing project, a monorepo may be the solution for you. Monorepos allow you to share dependencies between similar projects. For example, your website may use your local packages to showcase the latest features, instead of depending on a released version; your contributors can also conveniently update the docs as they implement features. An example monorepo folder structure is below:

```bash
my-monorepo
├── package-a # Another package, your actual project
│   ├── src
│   └── package.json # Package A's dependencies
├── website   # Docusaurus root
│   ├── docs
│   ├── src
│   └── package.json # Docusaurus' dependencies
├── package.json # Monorepo's shared dependencies
```

In this case, you should run `npx create-docusaurus` within the `./my-monorepo` folder.

If you're using a hosting provider such as Netlify or Vercel, you will need to change the `Base directory` of the site to where your Docusaurus root is. In this case, that would be `./website`. Read more about configuring ignore commands in the [deployment docs](./deployment.mdx#deploying-to-netlify).

Read more about monorepos in the [Yarn documentation](https://yarnpkg.com/features/workspaces) (Yarn is not the only way to set up a monorepo, but it's a common solution), or checkout [Docusaurus](https://github.com/facebook/docusaurus) and [Jest](https://github.com/facebook/jest) for some real-world examples.

## Running the development server {#running-the-development-server}

To preview your changes as you edit the files, you can run a local development server that will serve your website and reflect the latest changes.

```bash npm2yarn
cd my-website
npm run start
```

By default, a browser window will open at http://localhost:3000.

Congratulations! You have just created your first Docusaurus site! Browse around the site to see what's available.

## Build {#build}

Docusaurus is a modern static website generator so we need to build the website into a directory of static contents and put it on a web server so that it can be viewed. To build the website:

```bash npm2yarn
npm run build
```

and contents will be generated within the `/build` directory, which can be copied to any static file hosting service like [GitHub pages](https://pages.github.com/), [Vercel](https://vercel.com/) or [Netlify](https://www.netlify.com/). Check out the docs on [deployment](deployment.mdx) for more details.

## Updating your Docusaurus version {#updating-your-docusaurus-version}

There are many ways to update your Docusaurus version. One guaranteed way is to manually change the version number in `package.json` to the desired version. Note that all `@docusaurus/`-namespaced packages should be using the same version.

import UpgradeGuide from '@site/src/components/UpgradeGuide';

<UpgradeGuide />

Then, in the directory containing `package.json`, run your package manager's install command:

```bash npm2yarn
npm install
```

To check that the update occurred successfully, run:

```bash npm2yarn
npx docusaurus --version
```

You should see the correct version as output.

Alternatively, if you are using Yarn, you can do:

```bash
yarn upgrade @docusaurus/core@latest @docusaurus/preset-classic@latest
```

:::tip

Use new unreleased features of Docusaurus with the [`@canary` npm dist tag](/community/canary)

:::

## Problems? {#problems}

Ask for help on [Stack Overflow](https://stackoverflow.com/questions/tagged/docusaurus), on our [GitHub repository](https://github.com/facebook/docusaurus), our [Discord server](https://discordapp.com/invite/docusaurus), or [Twitter](https://twitter.com/docusaurus).

---

sidebar_position: 0
slug: /api/misc/create-docusaurus

---

# 📦 create-docusaurus

https://docusaurus.io/docs/api/misc/create-docusaurus

https://raw.githubusercontent.com/facebook/docusaurus/main/website/docs/api/misc/create-docusaurus.md

A scaffolding utility to help you instantly set up a functional Docusaurus app.

## Usage {#usage}

```bash
npx create-docusaurus@latest [name] [template] [rootDir]
```

The `name` argument will be used as the site's path as well as the `name` field in the created app's package.json. It can be an absolute path, or a path relative to `rootDir`.

The `template` argument can be one of the following:

- `classic`: Uses the classic template (recommended)
- `facebook`: Uses the Facebook/Meta template, which contains some Meta-specific setup
- A git repo URL (beginning with `https://` or `git@`), which can be cloned to the destination
- A local file path relative to CWD, which contains the files to be copied to destination

The `rootDir` will be used to resolve the absolute path to the site directory. The default is CWD.

:::caution

This command should be preferably used in an interactive shell so all features are available.

:::

## Options {#options}

### `-t, --typescript` {#typescript}

Used when the template argument is a recognized name. Currently, only `classic` provides a TypeScript variant.

### `-g, --git-strategy` {#git-strategy}

Used when the template argument is a git repo. It needs to be one of:

- `deep`: preserves full git history
- `shallow`: clones with `--depth=1`
- `copy`: does a shallow clone, but does not create a git repo
- `custom`: enter your custom git clone command. We will prompt you for it. You can write something like `git clone --depth 10`, and we will append the repository URL and destination directory.

### `-p, --package-manager` {#package-manager}

Value should be one of `npm`, `yarn`, or `pnpm`. If it's not explicitly provided, Docusaurus will infer one based on:

- The lockfile already present in the CWD (e.g. if you are setting up website in an existing project)
- The command used to invoke `create-docusaurus` (e.g. `npm init`, `npx`, `yarn create`, etc.)
- Interactive prompting, in case all heuristics are not present

### `-s, --skip-install` {#skip-install}

If provided, Docusaurus will not automatically install dependencies after creating the app. The `--package-manager` option is only useful when you are actually installing dependencies.

## Check NPM to see what are the latest packages

https://www.hostingadvice.com/how-to/update-npm-packages/

```
npm outdated
```

Output

```
Package                          Current  Wanted  Latest  Location                                      Depended by
@docusaurus/core                   2.0.1   2.0.1   2.1.0  node_modules/@docusaurus/core                 docusaurus-classic-site
@docusaurus/module-type-aliases    2.0.1   2.0.1   2.1.0  node_modules/@docusaurus/module-type-aliases  docusaurus-classic-site
@docusaurus/preset-classic         2.0.1   2.0.1   2.1.0  node_modules/@docusaurus/preset-classic       docusaurus-classic-site
@mdx-js/react                     1.6.22  1.6.22   2.1.3  node_modules/@mdx-js/react                    docusaurus-classic-site
react                             17.0.2  17.0.2  18.2.0  node_modules/react                            docusaurus-classic-site
react-dom                         17.0.2  17.0.2  18.2.0  node_modules/react-dom                        docusaurus-classic-site
typescript                         4.7.4   4.8.4   4.8.4  node_modules/typescript                       docusaurus-classic-site
```

## Update NPM to latest packages

```
npm update
```

Output

```
added 12 packages, removed 4 packages, changed 85 packages, and audited 1094 packages in 1m

197 packages are looking for funding
  run `npm fund` for details

21 vulnerabilities (8 moderate, 13 high)

To address issues that do not require attention, run:
  npm audit fix

Some issues need review, and may require choosing
a different dependency.

Run `npm audit` for details.
```

## Added plugin-ideal-image

https://docusaurus.io/docs/api/plugins/@docusaurus/plugin-ideal-image
