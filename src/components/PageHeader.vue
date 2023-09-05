<script setup>
import { useRoute } from 'vue-router'

const route = useRoute()
</script>

<template>
  <header class="">
    <div class="bg-blue-theme px-5 py-7">
      <div class="mx-auto flex max-w-screen-xl items-center justify-between gap-x-[5%]">
        <RouterLink to="/"
          ><img alt="Logo" src="@/assets/logo.svg" class="w-9/12 lg:w-full"
        /></RouterLink>

        <nav class="hidden w-full justify-between lg:flex">
          <RouterLink to="/" class="nav-link">Home</RouterLink>
          <RouterLink to="/" class="nav-link">Home</RouterLink>
          <RouterLink to="/" class="nav-link">Home</RouterLink>
          <RouterLink to="/" class="nav-link">Home</RouterLink>
          <!-- <RouterLink
            to="/about-me"
            :class="`text-base font-medium ${
              route.path === '/about-me' && 'border-b-orange border-b-2'
            }`"
            >About Me</RouterLink
          >
          <RouterLink
            to="#"
            :class="`text-base font-medium ${
              route.path === '/contact-me' && 'border-b-orange border-b-2'
            }`"
            >Contact Me</RouterLink
          > -->
        </nav>

        <RouterLink to="/" class="register-btn"> Register now </RouterLink>
      </div>
    </div>
  </header>
</template>
