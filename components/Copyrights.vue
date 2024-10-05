<script setup>
import { ref, onMounted } from 'vue'

const currentYear = ref(null);

onMounted(() => {
    currentYear.value = new Date().getFullYear();
});
</script>

<template>
    <section class="mt-20 pt-1">
        <hr class="mx-3 border-neutral-700">
        <div class="text-center text-neutral-400 py-6">
            © {{currentYear}}. All rights reserved.
        </div>
    </section>
</template>