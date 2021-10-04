<template>
  <div class="main-container w-full h-full bg-cover mx-auto flex flex-col relative text-white">
    <video autoplay muted loop class="w-screen absolute object-cover h-screen z-0">
      <source src="~/static/background/coming-soon-bg.mp4" type="video/mp4">
      <!-- https://www.pexels.com/video/digital-formation-of-a-dna-in-an-animated-presentation-3191572/ -->
      Your browser does not support the video tag.
    </video>
    <div class="w-full h-full absolute inset-0 bg-black bg-opacity-80">
      <span class="hidden">background opacity</span>
    </div>
    <div class="m-auto z-10 text-center">
      <div>
        <h1 class="text-4xl md:text-7xl">
          Coming soon
        </h1>
        <p class="mt-2">
          Personal page is still under development.
        </p>
      </div>
      <a class="border hover:bg-white hover:text-black duration-500 w-max mx-auto p-4 z-10 mt-8 block" href="https://media-exp1.licdn.com/media/AAYUBAR3AAgAAQAAAAAAADIDcMYD3UctSZ2lq1Ohvhr6lg.png" target="_blank">
        View resume
      </a>
    </div>
  </div>
</template>

<script lang="ts">
import Vue from 'vue'

export default Vue.extend({
})
</script>

<style lang="scss" scoped>
.main-container {
  background-image: url('~/static/background/coming-soon-bg.png');
}
</style>
