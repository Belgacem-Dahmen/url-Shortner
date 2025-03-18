<template>
  <img :alt="alt" :width="width" :height="height" class="logo" src="@/assets/images/logo.svg" />
</template>

<script setup lang="ts">


const props = defineProps({
  width: {
    type: [Number, String] as PropType<number | string>,
    required: true,
  },
  height: {
    type: [Number, String] as PropType<number | string>,
    required: true,
  },
  alt: {
    type: String,
    default: 'Vue logo',
  },
})
</script>

<style scoped>
.logo {
  display: flex;
  width: 125px;
  height: auto;
}
</style>
