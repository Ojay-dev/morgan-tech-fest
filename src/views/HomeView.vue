<script setup>
import TeamworkIcon from '@/components/icons/IconTeamwork.vue'
import ConferenceIcon from '@/components/icons/IconConference.vue'
import PurpleGlitterIcon from '@/components/icons/IconPurpleGlitter.vue'
import YellowGlitterIcon from '@/components/icons/IconYellowGlitter.vue'
import SmallPurpleGlitterIcon from '@/components/icons/IconSmPurpleGlitter.vue'
import SmallYellowGlitterIcon from '@/components/icons/IconSmYellowGlitter.vue'
</script>

<template>
  <div>
    <div class="hidden bg-blue-theme pb-[386px] pt-14 lg:block">
      <div class="mx-auto lg:max-w-5xl">
        <div class="hero-grid">
          <span class="hero-text">Discover</span>
          <div class="mx-auto"><PurpleGlitterIcon /></div>
          <div><TeamworkIcon /></div>
        </div>

        <div class="hero-grid">
          <div><ConferenceIcon /></div>
          <div class="mx-auto"><YellowGlitterIcon /></div>
          <span class="hero-text">Network</span>
        </div>

        <div class="hero-grid">
          <span class="hero-text">Innovate</span>
          <div class="mx-auto"><PurpleGlitterIcon /></div>

          <div class="flex gap-x-10">
            <div class="max-w-[163px]">
              <span class="font-Urbanist text-base font-black uppercase text-[#F68F21]">Date:</span>
              <p class="font-Urbanist text-[22px] text-white">Thurs Nov 16, Fri Nov 17, 2023</p>
            </div>
            <div class="max-w-[163px]">
              <span class="font-Urbanist text-base font-black uppercase text-[#F68F21]"
                >Venue:</span
              >
              <p class="font-Urbanist text-[22px] text-white">Calvin & Tina Tyler Ballroom</p>
            </div>
          </div>
        </div>
      </div>
    </div>

    <div class="block h-screen bg-blue-theme pt-8 lg:hidden">
      <div class="px-6 lg:px-0">
        <div class="hero-grid">
          <span class="hero-text">Discover</span>

          <div class="mx-auto"><SmallPurpleGlitterIcon /></div>

          <span class="hero-text">Network</span>

          <div class="mx-auto"><SmallYellowGlitterIcon /></div>

          <span class="hero-text">Innovate</span>

          <div class="mx-auto"><SmallPurpleGlitterIcon /></div>

          <div class="flex gap-x-10">
            <div class="max-w-[163px]">
              <span class="font-Urbanist text-base font-black uppercase text-[#F68F21]">Date:</span>
              <p class="font-Urbanist text-[22px] text-white">Thurs Nov 16, Fri Nov 17, 2023</p>
            </div>
            <div class="max-w-[163px]">
              <span class="font-Urbanist text-base font-black uppercase text-[#F68F21]">Date:</span>
              <p class="font-Urbanist text-[22px] text-white">Thurs Nov 16, Fri Nov 17, 2023</p>
            </div>
          </div>
        </div>
      </div>
    </div>
  </div>

  <div class="mx-auto px-6 lg:max-w-4xl lg:px-0">
    <div class="video-container">
      <iframe
        src="https://www.youtube.com/embed/vBqOMLd1ZQk"
        title="8 Surprising Habits that Got Me Millions of Subscribers"
        frameborder="0"
        allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share"
        allowfullscreen
      ></iframe>
    </div>
  </div>
</template>

<style scoped>
.hero-grid {
  @apply relative grid items-center justify-center gap-y-4 lg:grid-cols-[384px_0.4fr_384px] lg:gap-y-0;
}

.hero-text {
  @apply block max-w-[376px] text-center font-Bebas text-8xl font-normal text-white lg:text-left lg:text-[112px];
}

.video-container {
  @apply relative -mt-[100px] h-0 w-full pb-[56.25%] lg:-mt-[325px];
}

.video-container iframe {
  @apply absolute left-0 top-0 h-full w-full rounded-[30px];
}
</style>
