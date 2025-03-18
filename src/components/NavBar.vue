<template>
  <header class="navbar">
    <div class="navabar__left">
      <Logo :width="150" :height="150" />
      <div class="navbar__left-links">
        <MainLink text="Features" to="/" />
        <MainLink text="Pricing" to="/" />
        <MainLink text="Ressources" to="/" />
      </div>
    </div>
    <div class="navabar__right">
      <MainLink text="Login" />
      <MainButton text="Sign up" form="rounded" />
    </div>
    <Icon :src="menuIcon" @click="toggleMenu" />
  </header>
  <MobileMenu v-if="isVisible" />
</template>
<script setup lang="ts">
import MainButton from '@/components/MainButton.vue'
import MainLink from '@/components/MainLink.vue'
import Logo from '@/components/Logo.vue'
import Icon from '@/components/Icon.vue'
import MobileMenu from '@/components/MobileMenu.vue'
const menuIcon = new URL('@/assets/images/menu.svg', import.meta.url).href
import { ref } from 'vue'
const isVisible = ref(false)
const toggleMenu = () => {
  isVisible.value = !isVisible.value
}
</script>
<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  padding: 20px;
  align-items: center;
}

.navabar__left {
  display: flex;
  gap: 35px;
  align-items: center;
}

.navbar__left-links {
  display: flex;
  gap: 25px;
}

.navabar__right {
  display: flex;
  gap: 35px;
  align-items: center;
}

@media screen and (max-width: 685px) {
  .navbar {
    padding: 20px;
  }
  .navbar__left-links {
    display: none;
  }
  .navabar__right {
    display: none;
  }
}
</style>
