<template>
  <NavBar/>
  <Home v-if="!isAuthenticated"/>
  <notSignedin v-else/>
  <Footer v-if="isAuthenticated"/>
  </template>
  
  <script setup>
  import {authentication} from '~/functions/useFirebase'
  const {isAuthenticated} = authentication()
  </script>
  
  