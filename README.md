<a href="https://vuecedent.kaimacmaster.co.uk/">
  <h1 align="center">Vuecedent</h1>
</a>

<p align="center">
  Building blocks for your Nuxt project
</p>

<p align="center">
  <a href="https://github.com/kaimacmaster/vuecedent">
    <img src="https://img.shields.io/github/stars/kaimacmaster/vuecedent?label=kaimacmaster%2Fvuecedent" alt="Vuecedent repo star count" />
  </a>
</p>

<p align="center">
  <a href="#introduction"><strong>Introduction</strong></a> ·
  <a href="#one-click-deploy"><strong>One-click Deploy</strong></a> ·
  <a href="#tech-stack--features"><strong>Tech Stack + Features</strong></a> ·
  <a href="#author"><strong>Author</strong></a>
  <a href="#credits"><strong>Credits</strong></a>
</p>

<br/>

## Introduction

Vuecedent is an opinionated collection of components, hooks, and utilities for your Nuxt.js project.

## One-click Deploy

You can deploy this template to Vercel with the button below:

[![Deploy with Vercel](https://vercel.com/button)](https://vercel.com/new/clone?repository-url=https%3A%2F%2Fgithub.com%2Fkaimacmaster%2Fvuecedent&project-name=vuecedent&repository-name=vuecedent&demo-title=Vuecedent&demo-description=An%20opinionated%20collection%20of%20components%2C%20hooks%2C%20and%20utilities%20for%20your%20Nuxt%20project.&demo-url=https%3A%2F%2Fvuecedent.dev&demo-image=https%3A%2F%2Fvuecedent.dev%2Fopengraph-image&env=GOOGLE_CLIENT_ID,GOOGLE_CLIENT_SECRET,NEXTAUTH_SECRET&envDescription=How%20to%20get%20these%20env%20variables%3A&envLink=https%3A%2F%2Fgithub.com%2Fkaimacmaster%2Fvuecedent%2Fblob%2Fmain%2F.env.example&stores=%5B%7B"type"%3A"postgres"%7D%5D)

You can also clone & create this repo locally with the following command:

```bash
npx create-next-app vuecedent --example "https://github.com/kaimacmaster/vuecedent"
```

## Tech Stack + Features

### Frameworks

- [Nuxt](https://nuxt.com/) – React framework for building performant apps with the best developer experience
- [Nuxt Auth](https://auth.nuxtjs.org/) – Handle user authentication with ease with providers like Google, Twitter, GitHub, etc.
- [Prisma](https://www.prisma.io/) – Typescript-first ORM for Node.js

### Platforms

- [Vercel](https://vercel.com/) – Easily preview & deploy changes with git
- [Vercel Postgres](https://vercel.com/postgres) – Serverless Postgres at the Edge

### UI

- [Tailwind CSS](https://tailwindcss.com/) – Utility-first CSS framework for rapid UI development
- [Lucide](https://lucide.dev/) – Beautifully simple, pixel-perfect icons
- [`next/font`](https://nextjs.org/docs/basic-features/font-optimization) – Optimize custom fonts and remove external network requests for improved performance
- [`ImageResponse`](https://beta.nextjs.org/docs/api-reference/image-response) – Generate dynamic Open Graph images at the edge
- [`vue-wrap-balancer`](https://github.com/wobsoriano/vue-wrap-balancer) – Simple Vue component that makes titles more readable

### Hooks and Utilities

- `useIntersectionObserver` –  React hook to observe when an element enters or leaves the viewport
- `useLocalStorage` – Persist data in the browser's local storage
- `useScroll` – React hook to observe scroll position ([example](https://github.com/kaimacmaster/vuecedent/blob/main/components/navbar.vue#L12))
- `nFormatter` – Format numbers with suffixes like `1.2k` or `1.2M`
- `capitalize` – Capitalize the first letter of a string
- `truncate` – Truncate a string to a specified length
- [`use-debounce`](https://www.npmjs.com/package/use-debounce) – Debounce a function call / state update

### Code Quality

- [TypeScript](https://www.typescriptlang.org/) – Static type checker for end-to-end typesafety
- [Prettier](https://prettier.io/) – Opinionated code formatter for consistent code style
- [ESLint](https://eslint.org/) – Pluggable linter for Nuxt and TypeScript

### Miscellaneous

- [Vercel Analytics](https://vercel.com/analytics) – Track unique visitors, pageviews, and more in a privacy-friendly way

## Author

- Kai Macmaster ([@kaimacmaster](https://twitter.com/kaimacmaster)

## Credits

Based on the work for Next.js Precedent by Steven Tey ([@steventey](https://twitter.com/steventey))
