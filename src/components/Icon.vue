<template>
  <img :src="src" :alt="alt" class="iconClass"></img>
</template>

<script setup lang="ts">

const props = defineProps({
  src: {
    type: String,
    required: true,
  },
  alt: {
    type: String,
    default: 'Icon',
  },
  iconClass: {
    type: String,
    default: '',
  },
})
</script>

<style scoped>
.iconClass {
  display: none;
  width: 25px;
}

@media screen and (max-width: 685px) {
  .iconClass {
    display: block;
    width: 25px;
    color: var(--color-neutral-grayish-violet);
    cursor: pointer;
  }
}
</style>
