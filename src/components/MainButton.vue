<script setup lang="ts">
import { defineProps, computed } from 'vue'

type ButtonForm = 'rounded' | 'square'

const props = defineProps<{ text: string; form: ButtonForm }>()

const buttonStyle = computed(() => ({
  padding: '10px 25px',
  borderRadius: props.form === 'rounded' ? '50px' : '10px',
  backgroundColor: 'var(--color-primary-cyan)',
  border: 'none',
  outline: 'none',
  overflow: 'hidden',
  color: '#fff',
  cursor: 'pointer',
  fontSize: '16px',
  fontWeight: '600',
}))
</script>

<template>
  <button :style="buttonStyle">
    {{ props.text }}
  </button>
</template>
