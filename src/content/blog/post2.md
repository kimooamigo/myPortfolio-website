---
title: "Astro Blog Website"
description: "📚 Openblog is an elegant, simple, and user-friendly blog. Focused on accessibility, SEO and performance."
pubDate: "Apr 21 2024"
heroImage: "/AstroBlog.webp"
tags: ["Asrtro", "React", "CSS", "HTML", "tinaCMS", "JS", "Tailwind CSS", "Node JS"]
---

<div align="center">

<h3 align="center">
 ⭐ Leave a star if you like this project! ⭐️
</h3>

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fdanielcgilibert%2Fblog-template)
[![Deploy to Netlify](https://www.netlify.com/img/deploy/button.svg)](https://app.netlify.com/start/deploy?repository=https://github.com/danielcgilibert/blog-template)

</div>

## 📌 Table Of Contents

1. [Demo](#-Demo)
2. [CMS](#-Tina-CMS)
3. [Features](#-Features)
4. [Roadmap](#-Roadmap)
5. [Stack](#-Stack)
6. [Running locally](#-Running-Locally)
7. [Configure](#-Configure)
8. [Categories](#-Adding-a-category)
9. [Posts](#-Adding-a-post)
10. [Draft](#-Activating-draft-mode)
11. [FrontMatter](#-Frontmatter)
12. [CLI](#-Commands)

## 💻 Demo

Check out the [Demo](https://drmohamedonia.com/blog.html), hosted on Vercel
<br/>

https://github.com/kimooamigo/AstroBlog/assets/44746462/56b8399e-cc5b-45a8-b9d2-d69833ecadb1

## 🦙 Tina CMS

By default, this template comes pre-configured with Tina CMS.

Now you can create your posts directly from the CMS without the need to do it manually.

If you decide to use Tina, it's not necessary to add any properties to the Markdown files, Tina does it automatically.

Example:

https://github.com/kimooamigo/AstroBlog/assets/44746462/51ae324c-d383-40be-9b16-db159d1af15d

The documentation for Tina CMS can be found [here](https://tina.io/docs/)

> Tina is completely optional, and you can remove it, and it will still function in the same way.

## 💪 Features:
    
- ✅ Minimal styling
- ✅ Mobile responsive
- ✅ 100/100 Lighthouse performance
- ✅ SEO-friendly with canonical URLs and OpenGraph data
- ✅ Sitemap support
- ✅ RSS Feed support
- ✅ Markdown & MDX support
- ✅ Syntax highlighting
- ✅ Image optimization
- ✅ Table of contents
- ✅ Dark mode
- ✅ Reading Time
- ✅ [Pagefind](https://pagefind.app/) static search library integration
- ✅ Related posts
- ✅ Share posts (Linkedin, twitter)
- ✅ Draft mode
- ✅ Copy code block
- ✅ CMS in the repository (Tina CMS)
- ✅ Pagination
- ✅ ViewTransition (new)

## 🛣️ Roadmap

- ❌ Add post author
- ❌ Add customization with colors
- ❌ Add filters for reading time, date...
- ❌ More sharing options
- ❌ Internationalization (i18n)

## ⚙️ Stack

- [**ASTRO** + **Typescript**](https://astro.build/) - Astro is the all-in-one web framework designed for speed.
- [**Tailwind CSS** + **Tailwind-Merge** + **clsx**](https://tailwindcss.com/) - Tailwind CSS is a utility-first CSS framework.
- [**Tabler Icons**](https://tabler-icons.io/i/) - A open source SVG icons.
- [**Eslint**](https://eslint.org/) - ESLint is an open source project that helps you find and fix problems.
- [**Prettier**](https://prettier.io/) - Code formatter.
- [**Search Library**](https://pagefind.app/) - Static search library integration.
- [**Motion**](https://motion.dev/) - Motion One is the smallest fully-featured animation library for the web.
- [**Tina CMS**](https://tina.io/) - CMS.

## 👨🏻‍💻 Running Locally

**Recommended extensions for VSCode:**

- [Tailwind CSS IntelliSense](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss).
- [Astro](https://marketplace.visualstudio.com/items?itemName=astro-build.astro-vscode).

1. Clone or [fork](https://github.com/kimooamigo/Astro-Blog/fork) the repository:

```bash
git clone github.com:danielcgilibert/Astro-Blog.git
```

2. Select Directory Path 

```bash
cd Asro-Blog
```

3. Install dependencies:

```bash
npm install
# or
yarn install
# or
pnpm install
```

4. Run the development server:

```bash
npm run dev
# or
yarn dev
# or
pnpm dev
```

## 📐 Configure

- Edit the configuration file **src/data/site.config.ts** for the basic blog metadata.
- Update the **astro.config.mjs** file at the root of the project with your own domain.
- Modify the files in the **/public** folder:
  - favicon
  - robots.txt -> update the Sitemap url to your own domain
  - open-graph -> the open-graph is the image that will be displayed when sharing the blog link. For posts, the preview image is the post cover.
- Edit the social networks in the Header component - **src/components/Header.astro**, change the URL to your social network.

## 🗂️ Adding a category

To add a new category to your blog, simply go to the src/data/categories.ts file and add it to the array.

Example:

```ts
export  const  CATEGORIES  =  [
'JavaScript',
'React',
'new category here'  <---
]  as  const
```

> 🚨 Zod checks whether the category is not correctly written or does not exist in the properties of the markdown document. **It will throw an error when building the application.** 🚨

## 📄 Adding a post

Adding a post is as simple as adding a .md or .mdx file to the blog folder at the path **src/content/blog**. The filename will be used to create the slug/URL of the page.

For example, if you have a file named **jsx-and-react.md**, it will be transformed into: **http://yourdomain.com/post/jsx-and-react/**

## 📝 Activating draft mode

To activate draft mode, add the property **draft: true** to the file, and it will no longer be displayed on the blog.

Example :

```ts
title: MacBook Pro 2022
description: 'The new MacBook Pro 2022 is here. With the Apple M2 chip, a new design, and more, the new MacBook Pro is the best laptop Apple has ever made.'
pubDate: 'Jul 02 2022'
heroImage: '../../assets/bg.jpg'
category: 'Category 1'
tags: ['JavaScript', 'css', 'HTML5', 'GitHub']
draft: true <---
```

## ⚡️ Frontmatter

## Required properties:

- Title
- Description
- pubDate
- heroImage (post cover)
- category (Choose a category from src/data/categories.ts)

## Optional properties:

- draft (no need to include it, by default it's false)
- tags

> The schema for posts is located at src/content/config.ts. You can modify any parameter, for example, by adding a maximum of 80 characters for titles: title: z.string().max(80).
> For more information, refer to the zod documentation.

## 🧞 Commands

All commands are run from the root of the project, from a terminal:

| Command                 | Action                                                                                                                           |
| :---------------------- | :------------------------------------------------------------------------------------------------------------------------------- |
| `npm install`          | Installs dependencies                                                                                                            |
| `npm run dev`          | Starts local dev server at `localhost:3000`                                                                                      |
| `npm run build`        | Build your production site to `./dist/`                                                                                          |
| `npm run preview`      | Preview your build locally, before deploying                                                                                     |
| `npm run format:check` | Check code format with Prettier                                                                                                  |
| `npm run format`       | Format codes with Prettier                                                                                                       |
| `npm run sync`         | Generates TypeScript types for all Astro modules. [Learn more](https://docs.astro.build/en/reference/cli-reference/#astro-sync). |
| `npm run lint`         | Lint with ESLint                                                                                                                 |
