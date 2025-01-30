<script setup lang="ts">
interface Props {
  dark?: boolean;
}

withDefaults(defineProps<Props>(), {
  dark: false,
});
</script>

<template>
  <div class="max-w-[800px] px-2 lg:px-8">
    <h2 :class="['text-3xl text-black lg:text-5xl font-bold lg:tracking-tight capitalize', { 'text-white text-center': dark }]">
      <slot></slot>
    </h2>
    <p v-if="$slots.description" class="text-md lg:text-xl opacity-50 mt-2 lg:mt-6">
      <slot name="description"></slot>
    </p>
  </div>
</template>
