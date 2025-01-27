<template>
  <div>
    <HeroContainer :image="image" />
    <p class="h2 ma-3 pa-3 text-center ma-auto max-width-90%">
      Allo Pizza ... Retrouvez le goût des saveurs !
    </p>
    <PizzasList v-if="products !== null" :products="products.pizzas" />
    <p class="h2 ma-3 pa-3 text-center ma-auto max-width-90%">L'avis des clients ...</p>
    <ClientTestimonial v-if="products !== null" :products="products.testimonial" />
  </div>
</template>

<script setup>
import image from '../public/assets/photos/hero-pizzas.jpeg';
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
