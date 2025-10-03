<script setup>
const emit = defineEmits({
  flipCart(payload) {
    return payload;
  },
  changeStatus(payload) {
    return payload;
  },
});

function flip() {
  emit("flipCart", "Переворот");
}
</script>
<template>
  <div class="cart" @click="flip">
    <div class="frame-cart">
      <div class="say">word</div>
    </div>
  </div>
</template>
<style scoped>
.cart {
  display: flex;
  align-items: center;
  justify-content: center;
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
  width: 212px;
  height: 320px;
  border: 1px solid var(--color-bg-main);
  border-radius: 12px;
}
.say {
  font-weight: 400;
  font-style: var(--font);
  font-size: 18px;
}
/* .number {
  padding: 25px;
}
.lable {
  padding: 25px;
} */
</style>
