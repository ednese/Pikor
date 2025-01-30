<script setup>
import { footerItems } from '../nav.ts'

const socialNetworks = [{
  img: '/img/logo_insta.svg',
  link: 'https://www.instagram.com/pikor_actus/',
}, {
  img: '/img/logo_linkedIn.svg',
  link: 'https://www.linkedin.com/company/pikor-actus',
}]
</script>

<template>
  <footer>
    <nav
      class="flex flex-col items-center bg-[#191919] text-white py-16 gap-6 lg:gap-12"
    >
      <div class="flex items-center gap-12">
        <NuxtLink href="/" class="flex items-center justify-between text-lg flex gap-2">
          <img
            src="/img/logo.svg"
            alt="Logo"
            class="rounded border-white border-2 "
            loading="eager"
            width="42"
            height="42"
          />
        </NuxtLink>
        <p class="text-center">
          © {{ new Date().getFullYear() }} PIKOR
        </p>
      </div>
      <div class="flex items-center gap-12">
        <NuxtLink v-for="({ img, link }) in socialNetworks" :to="link" target="_blannk"
          class="flex items-center justify-between text-lg flex gap-2 p-3 rounded-full border-[#303030] border-2"
        >
          <img
            :src="img"
            alt="social img"
            loading="eager"
            width="12"
            height="12"
          />
        </NuxtLink>
      </div>
      <ul class="flex flex-col lg:flex-row text-center gap-4 lg:gap-8">
        <li v-for="item of footerItems">
          <NuxtLink
            :href="item.path"
          >
            {{ item.title }}
          </NuxtLink>
        </li>
      </ul>
    </nav>
  </footer>
</template>
