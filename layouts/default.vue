<template>
  <div>
    <div
      class="fixed h-screen w-full bg-gradient-to-br from-green-100 via-white to-emerald-200 dark:from-green-800 dark:via-green-900 dark:to-emerald-800"
    />
    <!-- <Nav /> -->
    <main
      class="flex min-h-screen w-full flex-col items-center justify-center py-32"
    >
      <slot />
    </main>
    <!-- <Footer /> -->
    <!-- Include Analytics as required -->
  </div>
</template>

<script setup lang="ts">
const head = {
  title: "Vuecedent - Building blocks for your Nuxt.js project",
  meta: [
    {
      hid: "description",
      name: "description",
      content:
        "Vuecedent is the all-in-one solution for your Nuxt project. It includes a design system, authentication, analytics, and more.",
    },
    {
      name: "twitter:card",
      content: "summary_large_image",
    },
    {
      name: "twitter:title",
      content: "Vuecedent - Building blocks for your Nuxt project",
    },
    {
      name: "twitter:description",
      content:
        "Vuecedent is the all-in-one solution for your Nuxt project. It includes a design system, authentication, analytics, and more.",
    },
    {
      name: "twitter:creator",
      content: "@steventey",
    },
  ],
  link: [{ rel: "icon", type: "image/x-icon", href: "/favicon.ico" }],
  htmlAttrs: {
    lang: "en",
  },
  bodyAttrs: {
    class: "your-body-class", // Add your appropriate body classes
  },
};

export { head };
</script>
