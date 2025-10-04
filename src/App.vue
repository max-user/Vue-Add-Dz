<script setup>
import { ref } from "vue";
import Score from "./components/Score.vue";
import Heart from "./icons/heart.vue";
import Cart from "./components/Cart.vue";

const datescore = ref({
  score: 100,
});

const datecart = ref({
  word: "Book",
  translation: "Книга",
  state: "closed",
  status: "pending",
});
</script>
<template>
  <main>
    <header class="header">
      <div class="text">Запомнить слово</div>
      <Score v-bind="datescore">
        <Heart />
      </Score>
    </header>
    <Cart v-bind="datecart"> </Cart>
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
