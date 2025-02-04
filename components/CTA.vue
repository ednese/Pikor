<script setup lang="ts">
interface Props {
  size?: 'md' | 'xl';
}

withDefaults(defineProps<Props>(), {
  size: 'md',
});
</script>

<template>
  <NuxtLink
    href="https://www.instagram.com/pikor_actus/"
    target="_blank"
    :class="['rounded font-medium text-center text-white bg-[#A39889] rounded-lg px-4 py-3 hover:bg-[#8B8072]',
      { 'lg:text-2xl lg:py-4 max-w-48 lg:max-w-72 w-full': size === 'xl' }]"
  >
    Suivre l’actu
  </NuxtLink>
</template>
