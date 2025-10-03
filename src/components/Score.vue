<script setup>
const { score } = defineProps({
  score: String,
});
</script>
<template>
  <div class="score">
    {{ score }}
    <slot></slot>
  </div>
</template>
<style scoped>
.score {
  display: flex;
  align-items: center;
  gap: 10px;
  width: 28;
  height: 24;
  font-weight: 700;
  color: var(--color-bg-main);
  background: #cce8ff;
  border-radius: 36px;
  padding: 12px 24px;
}
</style>
