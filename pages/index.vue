<template>
  <div>
    <HeroContainer :image="image" />
    <p class="h2 ma-3 pa-3 text-center ma-auto max-width-90%">
      Allo Pizza ... Retrouvez le goût des saveurs !
    </p>
    <FilterComponent
      v-if="products !== null"
      :products="products.pizzas"
      @update-category="filterPizzas"
    />
    <PizzasList v-if="products !== null" :products="filteredProducts" />
    <p class="h2 ma-3 pa-3 text-center ma-auto max-width-90%">L'avis des clients ...</p>
    <ClientTestimonial v-if="products !== null" :products="products.testimonial" />
  </div>
</template>

<script setup>
import image from '../public/assets/photos/hero-pizzas.jpeg';
import { onMounted, ref } from 'vue';
import FilterComponent from '../components/FilterComponent.vue';
import PizzasList from '../components/PizzasList.vue';
import ClientTestimonial from '../components/ClientTestimonial.vue';

const products = ref(null);
const filteredProducts = ref([]);

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
      filteredProducts.value = data.pizzas; // Initialize filteredProducts with all pizzas
    });
});

const filterPizzas = (category) => {
  if (category === 'all') {
    filteredProducts.value = products.value.pizzas;
  } else {
    filteredProducts.value = products.value.pizzas.filter(
      (product) => product.category === category,
    );
  }
};
</script>

<style scoped>
.h2 {
  font-size: clamp(1rem, 1.8vw, 2rem);
  font-weight: bold;
}
</style>
