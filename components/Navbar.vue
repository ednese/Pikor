<script setup>
import { items } from '../nav.ts'
</script>

<template>
  <header class="z-10 fixed w-full bg-[#DFDFDF] flex justify-between items-center px-6 py-4">
    <NuxtLink href="/" class="flex items-center justify-between text-lg flex gap-2">
      <img
        src="/img/logo.svg"
        alt="Logo"
        class="rounded"
        loading="eager"
        width="42"
        height="42"
      />
    </NuxtLink>
    <nav
      class="flex sm:block hidden"
    >
      <ul class="flex gap-3">
        <li v-for="item of items">
          <NuxtLink
            :href="item.path"
            class="flex px-3 py-2 text-gray-600 hover:text-gray-900"
          >
            {{ item.title }}
          </NuxtLink>
        </li>
      </ul>
    </nav>
    <div class="flex items-center gap-4">
      <CTA/>
    </div>
  </header>
</template>
