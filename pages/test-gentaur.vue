<template>
    <div class="post-list">
      <h1>Test Gentaur Page</h1>
      <div v-for="post in posts" :key="post.id" class="post-item">
        <div class="post-header">
          <h2>{{ post.title }}</h2>
          <p class="post-id">Post ID: {{ post.id }} | User ID: {{ post.userId }}</p>
        </div>
        <p class="post-body">{{ post.body }}</p>
      </div>
      <NuxtLink to="/" class="back-link">Back to Home</NuxtLink>
    </div>
  </template>
  
  <script setup>
  const { data: posts, error } = await useFetch('https://jsonplaceholder.typicode.com/posts');
  
    // Set the page title dynamically
    useHead({
      title: 'Test Gentaur Page'
      })
  if (error.value) {
    console.error('Error fetching posts:', error.value);
  }
  </script>
  