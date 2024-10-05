<script setup>
import { ref } from 'vue'

const linkedIn = ref('https://www.linkedin.com/in/jonaspaq/');
const gmail = ref('mailto:jonaspaq@gmail.com');
const github = ref('https://github.com/jonaspaq');

</script>

<template>
    <section class="mt-20" id="socials">
        <div class="text-center text-xl lg:text-2xl text-zinc-300 mx-6">
            Want to build software together? Connect with me.
        </div>
        <div class="flex flex-row items-center justify-center mt-5">
            <div class="mx-3">
                <a v-bind:href="linkedIn" target="_blank">
                    <img src="/images/linkedin.png" class="w-10" alt="LinkedIn">
                </a>
            </div>
            <div class="mx-3">
                <a v-bind:href="gmail">
                    <img src="/images/gmail.png" class="w-10" alt="Gmail">
                </a>
            </div>
            <div class="mx-3">
                <a v-bind:href="github" target="_blank">
                    <img src="/images/github.png" class="w-10" alt="Github">
                </a>
            </div>
        </div>
    </section>
</template>