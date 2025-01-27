<template>
  <div>
    <HeroContainer :image="image" />
    <DrinksList v-if="products !== null" :products="products.desserts" />
  </div>
</template>

<script setup>
import DrinksList from '~/components/DessertsList.vue';
import image from '../public/assets/photos/hero-desserts.jpg';
import { onMounted, ref } from 'vue';

const products = ref(null);

onMounted(() => {
  fetch('/allopizza.json')
    .then((response) => {
      if (response.ok) {
        return response.json();
      }
      throw new Error('Impossible de récupérer le JSON');
    })
    .then((data) => {
      products.value = data;
    });
});
</script>

<style scoped>
.h2 {
  font-size: clamp(1rem, 1.8vw, 2rem);
  font-weight: bold;
}
</style>
