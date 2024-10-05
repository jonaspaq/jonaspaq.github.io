<script setup>
  import { onMounted, onUnmounted, ref } from "vue";

  let scrollTopButton = ref(null);

  const handleScroll = () => {
    if (window.scrollY > 500) {
      scrollTopButton.value.classList.remove("invisible");
    } else {
      scrollTopButton.value.classList.add("invisible");
    }
  };

  function scrollToTop() {
    window.scrollTo({ top: 0, behavior: "smooth" });
  }

  onMounted(() => {
    handleScroll()
    window.addEventListener("scroll", handleScroll);
  });

  onUnmounted(() => {
    window.removeEventListener("scroll", handleScroll);
  });
</script>

<template>
    <div ref="scrollTopButton" class="sticky w-full flex justify-end bottom-0 pb-3 pr-5 transition invisible">
        <div class="text-gray-400 hover:text-blue-400 transition">
            <button @click="scrollToTop"
                class="rounded-full border-2 border-zinc-400 p-3">
                <svg xmlns="http://www.w3.org/2000/svg" class="fill-primary w-4 h-4" viewBox="0 0 384 512">
                    <path d="M214.6 9.4c-12.5-12.5-32.8-12.5-45.3 0l-128 128c-12.5 12.5-12.5 32.8 0 45.3s32.8 12.5 45.3 0L160 109.3 160 480c0 17.7 14.3 32 32 32s32-14.3 32-32l0-370.7 73.4 73.4c12.5 12.5 32.8 12.5 45.3 0s12.5-32.8 0-45.3l-128-128z"/>
                </svg>
            </button>
        </div>
    </div>
</template>