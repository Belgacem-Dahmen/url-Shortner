<template>
  <div class="mobileMenu">
    <MainLink text="Features" to="/" />
    <MainLink text="Pricing" to="/" />
    <MainLink text="Ressources" to="/" />
  </div>
</template>

<script setup lang="ts">
import MainLink from '@/components/MainLink.vue'
</script>

<style scoped>
.mobileMenu {
  background-color: var(--color-primary-dark-violet);
  max-width: 100%;
  margin: 5px 15px;
  padding: 50px 0;
  border-radius: 10px;
  display: none;
  flex-direction: column;
  gap: 35px;
  align-items: center;
}

@media screen and (max-width: 675px) {
  .mobileMenu {
    display: flex;
  }
}
</style>
