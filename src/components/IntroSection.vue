<template>
  <div class="IntroSection">
    <div class="text-section">
      <h1 class="title">More than just shorter links</h1>
      <p class="text">
        Build your brand’s recognition and get detailed insights on how your links are performing.
      </p>
      <MainButton text="Get Started" form="rounded" />
    </div>
  </div>
</template>

<script setup lang="ts">
import MainButton from '@/components/MainButton.vue'
</script>

<style scoped>
.text-section {
  background: url('@/assets/images/illustration-working.svg');
  background-repeat: no-repeat;
  background-position: right;
  background-size: 50%;
}
.IntroSection {
  margin-top: 100px;
}
.title {
  font-size: 4.5rem;
  max-width: 600px;
  line-height: 4rem;
  margin-bottom: 20px;
}
.text {
  color: var(--color-neutral-grayish-violet);
  font-size: 1.325rem;
  max-width: 500px;
  margin-bottom: 25px;
}
</style>
