<template>
    <div class="homepage">
      <h1 class="title">Welcome to the Nuxt SSR Homepage</h1>
      <NuxtLink to="/test-gentaur" class="link">Go to Test Page</NuxtLink>
    </div>
  </template>
 <script setup>
 import { useHead } from '#app'
 
 const pageTitle = 'Welcome to the Nuxt SSR Homepage'
 
 // Dynamically set the page title using useHead
 useHead({
   title: pageTitle
 })
 </script>