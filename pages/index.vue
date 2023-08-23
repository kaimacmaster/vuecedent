<template>
  <div class="z-10 w-full max-w-xl px-5 xl:px-0">
    <a
      href="https://twitter.com/steventey/status/1613928948915920896"
      target="_blank"
      rel="noreferrer"
      class="mx-auto mb-5 flex max-w-fit animate-fade-up items-center justify-center space-x-2 overflow-hidden rounded-full bg-blue-100 px-7 py-2 transition-colors hover:bg-blue-200"
    >
      <!-- <Twitter class="h-5 w-5 text-[#1d9bf0]" /> -->
      <p class="text-sm font-semibold text-[#1d9bf0]">Introducing Vuecedent</p>
    </a>
    <h1
      class="animate-fade-up bg-gradient-to-br from-black to-stone-500 bg-clip-text text-center font-display text-4xl font-bold tracking-[-0.04em] text-transparent drop-shadow-sm md:text-7xl md:leading-[5rem]"
    >
      <WrapBalancer>Building blocks for your Nuxt project</WrapBalancer>
    </h1>
    <p
      class="mt-6 animate-fade-up text-center text-gray-500 dark:text-gray-300 md:text-xl"
    >
      <WrapBalancer>
        An opinionated collection of components, hooks, and utilities for your
        Nuxt project.
      </WrapBalancer>
    </p>
    <div
      class="mx-auto mt-6 flex animate-fade-up items-center justify-center space-x-5"
    >
      <a
        class="group flex max-w-fit items-center justify-center space-x-2 rounded-full border border-black bg-black px-5 py-2 text-sm text-white transition-colors hover:bg-white hover:text-black"
        :href="DEPLOY_URL"
        target="_blank"
        rel="noopener noreferrer"
      >
        <!-- Your SVG here -->
        <p>Deploy to Vercel</p>
      </a>
      <a
        class="flex max-w-fit items-center justify-center space-x-2 rounded-full border border-gray-300 bg-white px-5 py-2 text-sm text-gray-600 shadow-md transition-colors hover:border-gray-800"
        href="https://github.com/kaimacmaster/vuecedent"
        target="_blank"
        rel="noopener noreferrer"
      >
        <!-- <Github /> -->
        <p>
          <span class="hidden sm:inline-block">Star on</span> GitHub
          <span class="font-semibold">{{ nFormatter(stars) }}</span>
        </p>
      </a>
    </div>
    <div
      class="my-10 grid w-full max-w-screen-xl animate-fade-up grid-cols-1 gap-5 px-5 md:grid-cols-3 xl:px-0"
    >
      <Card
        v-for="feature in features"
        :key="feature.title"
        :title="feature.title"
        :description="feature.description"
        :demo="feature.demo"
        :large="feature.large"
      />
    </div>
  </div>
</template>

<script setup>
// import Card from "@/components/home/card";
// import Github from "@/components/shared/icons/Github.vue";
// import Twitter from "@/components/shared/icons/Twitter.vue";
import { DEPLOY_URL } from "@/lib/constants";
import { nFormatter } from "@/lib/utils";
import WrapBalancer from "vue-wrap-balancer";

import { onMounted, ref } from "vue";
// Define your DEPLOY_URL and nFormatter function

const stars = ref(0);
const features = [
  {
    title: "Beautiful, reusable components",
    description:
      "Pre-built beautiful, a11y-first components, powered by [Tailwind CSS](https://tailwindcss.com/), [Radix UI](https://www.radix-ui.com/), and [Framer Motion](https://framer.com/motion)",
    large: true,
  },
  {
    title: "Performance first",
    description:
      "Built on [Nuxt](https://nextjs.org/) primitives like `@next/font` and `next/image` for stellar performance.",
    demo: "web-vitals",
  },
  {
    title: "One-click Deploy",
    description:
      "Jumpstart your next project by deploying Vuecedent to [Vercel](https://vercel.com/) in one click.",
    demo: {
      type: "image-link",
      src: "https://vercel.com/button",
      alt: "Deploy with Vercel",
      width: 120,
      height: 30,
    },
  },
  {
    title: "Built-in Auth + Database",
    description:
      "Vuecedent comes with authentication and database via [Auth.js](https://authjs.dev/) + [Prisma](https://prisma.io/)",
    demo: "auth-database",
  },
  {
    title: "Hooks, utilities, and more",
    description:
      "Vuecedent offers a collection of hooks, utilities, and `@vercel/og`",
    demo: "utilities",
  },
];

onMounted(async () => {
  try {
    const response = await fetch(
      "https://api.github.com/repos/kaimacmaster/vuecedent",
      {
        headers: process.env.GITHUB_OAUTH_TOKEN
          ? {
              Authorization: `Bearer ${process.env.GITHUB_OAUTH_TOKEN}`,
              "Content-Type": "application/json",
            }
          : {},
      }
    );
    const { stargazers_count } = await response.json();
    stars.value = stargazers_count;
  } catch (e) {
    console.log(e);
  }
});
</script>
