<template>
  <div class="h-screen flex flex-col bg-black relative px-1">
    <div class="fixed w-full z-10">
      <nav class="container mx-auto flex flex-col text-center sm:flex-row sm:text-left sm:justify-between py-4 px-6 shadow sm:items-baseline w-full bg-transparent">
        <div class="mb-2 sm:mb-0">
          <a href="/" class="text-xl no-underline text-gray-400 bg-opacity-90 hover:text-blue-dark">Jonas Paquibot</a>
        </div>
        <div>
          <a href="https://www.linkedin.com/in/jonaspaq/" target="_blank" class="text-sm no-underline text-gray-400 bg-opacity-90 hover:text-white ml-2">LinkedIn</a>
          <a href="https://github.com/jonaspaq" target="_blank" class="text-sm no-underline text-gray-400 bg-opacity-90 hover:text-white ml-2">Github</a>
        </div>
      </nav>
    </div>

    <Nuxt class="h-full" />
  </div>
</template>
