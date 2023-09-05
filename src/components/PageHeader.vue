<script setup>
// import { useRoute } from 'vue-router'
import ChocolateMenuIcon from '@/components/icons/IconChocolateMenu.vue'

import { ref, computed, watch } from 'vue'
import { AppstoreOutlined } from '@ant-design/icons-vue'
// const route = useRoute()

const isClicked = ref(false)

const scaleDown = () => {
  isClicked.value = true
  setTimeout(() => {
    isClicked.value = false
  }, 200)
}

const buttonClass = computed(() => ({
  'register-btn': true,
  clicked: isClicked.value
}))

// Antd menu functions
const selectedKeys = ref(['1'])
const openKeys = ref([''])

const isMenuOpen = ref(false)

const titleClick = (e) => {
  console.log('titleClick', e)
}

const handleClick = (e) => {
  console.log('click', e)
  openKeys.value = ['']
}

const toggleMenu = () => {
  isMenuOpen.value = !isMenuOpen.value
}

watch(isMenuOpen, (val) => {
  if (val) {
    openKeys.value = ['sub2']
  } else {
    openKeys.value = ['']
  }
})
</script>

<template>
  <header class="bg-blue-theme">
    <div class="header-bg px-5 py-7">
      <div class="mx-auto flex max-w-screen-xl items-center justify-between gap-x-[5%]">
        <div class="flex items-center gap-x-3">
          <button class="md:hidden" @click="toggleMenu"><ChocolateMenuIcon /></button>
          <RouterLink to="/"
            ><img alt="Logo" src="@/assets/logo.svg" class="w-9/12 lg:w-full"
          /></RouterLink>
        </div>

        <nav class="hidden w-full max-w-screen-sm justify-between md:flex">
          <RouterLink to="/" class="nav-link">Home</RouterLink>
          <RouterLink to="/" class="nav-link">About us</RouterLink>
          <RouterLink to="/" class="nav-link">Schedule</RouterLink>
          <RouterLink to="/" class="nav-link">Speakers</RouterLink>
          <RouterLink to="/" class="nav-link">Sponsors</RouterLink>
          <RouterLink to="/" class="nav-link">FAQ</RouterLink>
        </nav>

        <RouterLink to="/" :class="buttonClass" @click="scaleDown">Register now</RouterLink>
      </div>
    </div>
  </header>

  <a-menu
    id="dddddd"
    v-model:openKeys="openKeys"
    v-model:selectedKeys="selectedKeys"
    mode="inline"
    @click="handleClick"
    class="antd-custom-menu"
  >
    <a-sub-menu key="sub2" @titleClick="titleClick">
      <template #icon>
        <AppstoreOutlined />
      </template>
      <template #title>Navigation Two</template>
      <a-menu-item key="Home">Home</a-menu-item>
      <a-menu-item key="About us">About us</a-menu-item>
      <a-menu-item key="Schedule">Schedule</a-menu-item>
      <a-menu-item key="Speakers">Speakers</a-menu-item>
      <a-menu-item key="Sponsors">Sponsors</a-menu-item>
      <a-menu-item key="FAQ">FAQ</a-menu-item>
    </a-sub-menu>
  </a-menu>
</template>

<style scoped>
.header-bg {
  /* border: 3px solid linear-gradient(136deg, rgba(255, 255, 255, 0.2), rgb(255, 255, 255)); */
  /*
  backdrop-filter: blur(3.3px);
  */
  border: 3px solid rgba(255, 255, 255, 0.014);
  background: linear-gradient(
      175deg,
      rgba(177, 177, 177, 0.32) 5.24%,
      rgba(54, 53, 103, 0.2) 51.01%
    ),
    rgba(0, 0, 128, 0.3);
}
.nav-link {
  @apply font-urbanist text-base font-medium text-white;
}

.register-btn {
  @apply flex h-[40px] w-full max-w-[165px] items-center justify-center rounded-[80px] px-9 text-sm font-extrabold text-[#121139] md:h-14 md:max-w-[196px] md:text-lg;
  background: linear-gradient(180deg, #fc711b 25.62%, #fc4608 100.89%);
}

.clicked {
  transform: scale(0.9);
}
</style>
