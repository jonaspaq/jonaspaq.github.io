<script setup>
const linkedIn = ref('https://www.linkedin.com/in/jonaspaq/');
</script>

<template>
    <section>
        <div class="flex flex-row flex-wrap items-center justify-center mt-20">
            <div class="w-full md:w-9/12">
                <div class="text-4xl md:text-7xl text-center lg:text-left">
                    <p>
                        Hi, I'm <span class="text-primary font-medium">{Jonas}</span>,
                    </p>
                     a software developer.
                </div>
            </div>
            <div class="w-full lg:w-2/12 flex flex-row items-center justify-center">
                <div class="relative mt-5 w-56 h-56 flex items-center justify-center">
                    <div class="bg-primary border-4 blur-2xl p-10 rounded-full w-36 h-36 absolute z-10 top-1/2 left-1/2 transform -translate-x-1/2 -translate-y-1/2">

                    </div>
                    <a :href="linkedIn" target="_blank" class="bg-zinc-900 py-3 px-10 z-20 relative rounded-sm hover:bg-opacity-90 cursor-pointer transition">
                        Contact me
                    </a>
                </div>
            </div>
        </div>
    </section>
</template>