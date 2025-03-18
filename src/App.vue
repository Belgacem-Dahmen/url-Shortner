<script setup lang="ts">
import { RouterLink, RouterView } from 'vue-router'
import NavBar from '@/components/Navbar.vue'
</script>

<template>
  <div class="container">
    <NavBar />
    <RouterView />
  </div>
</template>

<style scoped></style>
