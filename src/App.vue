<script setup>
import Score from "./components/Score.vue";
import Heart from "./icons/heart.vue";
import Cart from "./components/Cart.vue";
</script>
<template>
  <main>
    <header class="header">
      <div class="text">Запомнить слово</div>
      <Score>
        Cчет
        <Heart />
      </Score>
    </header>
    <Cart> </Cart>
  </main>
</template>
<style scoped>
.header {
  padding: 0 66px;
  display: flex;
  align-items: center;
  justify-content: space-between;
  width: 100%;
  height: 121px;
}
.text {
  height: 24px;
  font-weight: 700;
  text-transform: uppercase;
  color: var(--color-bg-main);
}
</style>
