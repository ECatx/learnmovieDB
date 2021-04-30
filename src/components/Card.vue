<template>
    <div class="max-w-full flex">
        <img src="https://via.placeholder.com/200x300.png" alt="movie poster">
        <div class="flex flex-col justify-between p-4 leading-normal bg-white border-b border-l border-r border-blueGray-400 rounded-b lg:border-l-0 lg:border-t lg:border-blueGray-400 lg:rounded-b-none lg:rounded-r">
            <div class="mb-8">
                <div class="mb-2 text-xl font-semibold text-blueGray-900">
                    Movie Title
                </div>
                <p class="text-base text-blueGray-700 line-clamp-6">
                    Lorem ipsum dolor sit amet consectetur adipisicing elit. Cupiditate delectus provident recusandae cumque laboriosam facilis voluptas id repellat quidem optio earum, quod facere accusamus praesentium eligendi in sapiente. Illo, hic?
                </p>
            </div>
            <div class="flex items-start justify-end">
                <div class="flex flex-col items-center">
                    <button class="text-blueGray-700 hover:text-rose-600" @click=""> 
                        <mdi:heart-plus class="w-8 h-8"/>
                        <span>{{7}}</span>
                    </button>
                </div>
                <div class="flex flex-col items-center pl-2">
                    <button  class="text-blueGray-700 hover:text-green-400" @click="toggle">
                        <bx:bxs-comment-add class="w-8 h-8" />
                    </button>
                </div>
            </div>
        </div>
    </div>
    <Comments v-if="value" @close="toggle"/>
</template>

<script setup>
  import {useToggle} from '@vueuse/core'
  const [value,toggle] = useToggle()
</script>