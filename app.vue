<script setup>
import { onMounted, onBeforeUnmount, ref } from 'vue'

const vantaBg = ref(null)
let vantaEffect = null

onMounted(() => {
  // Dynamically load three.js and Vanta Waves script
  loadVanta()
})

const loadVanta = () => {
  const threeScript = document.createElement('script')
  threeScript.src = 'https://cdnjs.cloudflare.com/ajax/libs/three.js/r134/three.min.js'
  threeScript.onload = () => {
    const vantaScript = document.createElement('script')
    vantaScript.src = 'https://cdn.jsdelivr.net/npm/vanta@latest/dist/vanta.birds.min.js'
    vantaScript.onload = initVanta
    document.head.appendChild(vantaScript)
  }
  document.head.appendChild(threeScript)
}

const initVanta = () => {
    vantaEffect = VANTA.BIRDS({
        el: vantaBg.value,
        mouseControls: true,
        touchControls: true,
        gyroControls: false,
        minHeight: 200.00,
        minWidth: 200.00,
        scale: 1.00,
        scaleMobile: 1.00,
        backgroundColor: 0x0B0B0B,
        color1: 0x07EA9A,
        color2: 0x07EA9A,
        birdSize: 1.30,
        quantity: 2.00
    })
}

onBeforeUnmount(() => {
  if (vantaEffect) vantaEffect.destroy()
})
</script>

<template>
  <div class="xl:container border-0 border-blue-500 mx-auto z-20">
    <div id="vanta-bg" ref="vantaBg">
      <AppNavbar />
      <AppHeader />
  
      <CompanyLogos />
    </div>
    <ExperienceHighlights />

    <ConnectWithMe />

    <Copyrights />

    <ScrollToTopButton />
  </div>
</template>

<style>
body {
  background-color: #0B0B0B;
  color: white;
  position: relative;
}
</style>