<script setup lang="ts">
import MarkdownIt from "markdown-it";
import { computed, ref } from "vue";

const props = defineProps<{
  title: string;
  description: string;
  large?: boolean;
}>();

const title = ref(props.title);
const description = ref(props.description);
const large = ref(props.large);

const markdown = new MarkdownIt();
const descriptionHtml = computed(() => markdown.render(props.description));

const cardClasses = computed(() => [
  "relative col-span-1 h-96 overflow-hidden rounded-xl border border-gray-200 bg-white shadow-md",
  large.value ? "md:col-span-2" : "",
]);
</script>

<template>
  <div :class="cardClasses">
    <div class="flex h-60 items-center justify-center">
      <slot name="demo"></slot>
    </div>
    <div class="mx-auto max-w-md text-center">
      <h2
        class="bg-gradient-to-br from-black to-stone-500 bg-clip-text font-display text-xl font-bold text-transparent md:text-3xl md:font-normal"
      >
        {{ title }}
      </h2>
      <div class="prose-sm -mt-2 leading-normal text-gray-500 md:prose">
        <WrapBalancer>
          <div v-html="descriptionHtml" />
        </WrapBalancer>
      </div>
    </div>
  </div>
</template>
