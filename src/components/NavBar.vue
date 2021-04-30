<template>
    <nav class="bg-gray-800">
        <div class="container mx-auto flex items-center justify-between shadow-xl">
            <div class="flex items-center space-x-5">
                <whh:movieclapper class="h-12 w-12 text-coolGray-500"/>
                <p class="text-4xl tracking-widest text-transparent font-light bg-clip-text bg-gradient-to-r from-rose-500 via-green-600 to-blue-700">Movies<span class="font-bold">DB</span></p>
            </div>
            <div>
                <div v-if="isAuthenticated" class="flex items-center space-x-5">
                  <p class="text-blueGray-400">Hello {{user?.displayName}}</p>
                  <button class="px-8 py-2 font-medium bg-purple-900 rounded-full focus:ring-pink-400 focus:ring-2 focus:outline-none text-blueGray-300 hover:bg-purple-700" @click="signOut">
                    Logout
                </button> 
                </div>
                <div v-else>
                    <button class="px-8 py-2 font-medium bg-blue-900 rounded-full focus:ring-yellow-400 focus:ring-2 focus:outline-none text-blueGray-300 hover:bg-blue-700" @click="googlePopup">
                        Login
                    </button>
                </div>
            </div>
        </div>
    </nav>
</template>

<script setup>
import {ref} from 'vue'
import {authentication} from '../functions/useFirebase'
const {googlePopup,signOut,isAuthenticated,user} = authentication()
</script>