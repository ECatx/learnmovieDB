<template>
    <footer class="bg-gray-900">
        <div class="container flex items-center justify-end px-3 py-5 mx-auto space-x-5 space-y-4 text-blueGray-400">
            <img :src="tmdb" class="w-12" alt="TMDB logo">
        </div>
    </footer>
</template>

<script setup>
    import tmdb from '../assets/tmdb.svg'
</script>