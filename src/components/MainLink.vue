<template>
  <router-link :to="props.to" class="main-link">
    <p>{{ props.text }}</p>
  </router-link>
</template>

<script setup lang="ts">
const props = defineProps<{
  text: string
  to: string
}>()
</script>

<style scoped>
.main-link {
  text-decoration: none;
  color: var(--color-neutral-grayish-violet);
}
p {
  font-weight: 600;
}
</style>
