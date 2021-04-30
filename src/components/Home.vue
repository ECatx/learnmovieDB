<template>
    <div class="container grid gap-3 mx-auto my-3 text-center lg:grid-cols-2">
        <Card v-for="(n,index) in 10" :key="index"/>
    </div>
    <div class="flex items-center justify-center mb-5 space-x-3">
        <div>
            <button class="px-4 py-2 bg-white rounded">Previous</button>
        </div>
        <div>
            <p class="px-4 text-blueGray-200">Page 1 of 10</p>
        </div>
        <div>
            <button class="px-4 py-2 bg-white rounded">
                Next
            </button>
        </div>
    </div>
</template>