<template>
  <header class="navbar">
    <div class="navabar__left">
      <img
        alt="Vue logo"
        class="navabar__left-logo"
        src="@/assets/images/logo.svg"
        width="125"
        height="125"
      />
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
  </header>
</template>
<script setup lang="ts">
import MainButton from '@/components/MainButton.vue'
import MainLink from '@/components/MainLink.vue'
</script>
<style scoped>
.navbar {
  display: flex;
  justify-content: space-between;
  padding-top: 35px;
  align-items: center;
}

.navabar__left {
  display: flex;
  gap: 35px;
  align-items: center;
}

.navabar__left-logo {
  display: flex;
  width: 125px;
  height: 100%;
}

.navbar__left-links {
  display: flex;
  gap: 25px;
}

.navabar__right {
  display: flex;
  gap: 35px;
  align-items: center;
  padding-right: 50px;
}
</style>
