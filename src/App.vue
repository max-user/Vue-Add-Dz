<script setup>
import { computed, ref } from "vue";
import Score from "./components/Score.vue";
import Heart from "./icons/heart.vue";
import Cart from "./components/Cart.vue";

const datescore = ref({
  score: "100",
});

const datecart = ref([
  {
    word: "Book",
    translation: "Книга",
    state: "closed",
    status: "pending",
  },
  {
    word: "Lesson",
    translation: "Урок",
    state: "closed",
    status: "pending",
  },
]);

const dataCartModified = computed(() => {
  return [
    {
      word: "Book",
      translation: "Книга",
      state: "closed",
      status: "pending",
    },
    {
      word: "Lesson",
      translation: "Урок",
      state: "closed",
      status: "pending",
    },
    {
      word: "Key",
      translation: "Ключ",
      state: "Open",
      status: "pending",
    },
    {
      word: "Edit",
      translation: "Редактировать",
      state: "closed",
      status: "pending",
    },
  ];
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
    <div class="carts">
      <Cart v-for="item in dataCartModified" :key="item.word" v-bind="item">
      </Cart>
    </div>
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
.carts {
  display: flex;
  align-items: center;
  justify-content: center;
  gap: 15px;
}
</style>
