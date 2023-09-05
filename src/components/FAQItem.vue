<script setup>
import ChevronDownIcon from '@/components/icons/IconChevronDown.vue'
import { ref } from 'vue'
const { question, answer } = defineProps(['question', 'answer'])

const CouroselOpened = ref(false)

function toggleRotation() {
  CouroselOpened.value = !CouroselOpened.value
}
</script>

<template>
  <div>
    <div
      class="flex cursor-pointer items-center justify-between border-b-[0.3px] border-[#ffffff89] py-3 lg:py-4"
      @click="toggleRotation"
    >
      <span class="text-2xl font-semibold text-white lg:text-3xl">{{ question }}</span>

      <span :class="{ 'rotate-90-open': CouroselOpened, 'rotate-90-close': !CouroselOpened }">
        <ChevronDownIcon />
      </span>
    </div>

    <p
      v-if="CouroselOpened"
      class="font-urbanist py-3 text-base font-normal text-white lg:py-4 lg:text-xl"
    >
      {{ answer }}
    </p>
  </div>
</template>

<style scoped>
.rotate-90-open {
  transform: rotate(-90deg);
  transition: transform 0.3s ease;
}
.rotate-90-close {
  transform: rotate(0deg);
  transition: transform 0.3s ease;
}
</style>
