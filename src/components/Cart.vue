<script setup>
import fail from "../icons/fail.vue";
import ok from "../icons/ok.vue";

const emit = defineEmits({
  flipCart(payload) {
    return payload;
  },
  changeStatus(payload) {
    return payload;
  },
});
const { word, translation, state, status } = defineProps({
  word: String,
  translation: String,
  state: String,
  status: String,
});
function flip() {
  emit("flipCart", "Переворот");
}
</script>
<template>
  <div class="cart" @click="flip">
    <div class="frame-cart">
      <div class="state">{{ state }}</div>
      <div class="say">{{ word }}</div>
      <div class="say">{{ translation }}</div>
      <div class="status">{{ status }}</div>
    </div>
    <div class="footer">
      <ok />
      <fail> </fail>
    </div>
  </div>
</template>
<style scoped>
.cart {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  /* padding: 8px 18px; */
  background: var(--color-bg-card);
  width: 250px;
  height: 376px;
  border-radius: 12px;
}
.frame-cart {
  display: flex;
  align-items: center;
  justify-content: center;
  flex-direction: column;
  width: 212px;
  height: 320px;
  border: 1px solid var(--color-bg-main);
  border-radius: 12px;

  height: 320;
}
.say {
  font-weight: 400;
  font-style: var(--font);
  font-size: 18px;
}
.footer {
  display: flex;
  justify-content: space-between;
  gap: 10px;
}
</style>
