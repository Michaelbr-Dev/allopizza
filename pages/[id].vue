<template>
  <div>
    <HeroContainer :image="image" />
    <PizzaDetails :pizza="pizza" />
  </div>
</template>

<script setup>
import image from '../public/assets/photos/hero-pizzas.jpeg';
import { ref } from 'vue';
import { useRoute } from 'vue-router';
import PizzaDetails from '~/components/PizzaDetails.vue';
import allopizzaData from '~/public/allopizza.json';

const route = useRoute();
const pizzaId = route.params.id;
const pizza = ref(allopizzaData.pizzas.find((p) => p.id === Number(pizzaId)));
</script>
