<template>
  <v-card variant="tonal" class="rounded-lg w-75 mx-auto my-7 text-center text-white">
    <v-card-title>{{ props.pizza.name }} - {{ props.pizza.price }}</v-card-title>
    <v-card-subtitle>{{ props.pizza.subName }}</v-card-subtitle>
    <v-card-text>{{ props.pizza.ingredients }}</v-card-text>
    <v-img class="ma-2 rounded-lg" :src="assetPath + props.pizza.img" />
  </v-card>
</template>

<script setup>
const assetPath = '/assets/pizzas/';
const props = defineProps({
  pizza: { type: Array, required: true },
});
</script>
