<template>
  <NavBar/>
  <Home v-if="isAuthenticated"/>
  <notSignedin v-else/>
  <Footer/>
  </template>
  
  <script setup>
  import {authentication} from '~/functions/useFirebase'
  const {isAuthenticated} = authentication()
  </script>
  
  