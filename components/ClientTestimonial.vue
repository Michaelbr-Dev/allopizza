<template>
  <div class="testimonial">
    <v-row justify="center">
      <v-col v-for="product in props.products" :key="product.id" lg="3">
        <v-sheet class="rounded-lg">
          <div class="pa-3">
            {{ product.text }}
          </div>
        </v-sheet>
      </v-col>
    </v-row>
  </div>
</template>

<script setup>
const props = defineProps({
  products: { type: Array, required: true },
});
console.log(props);
</script>

<style scoped>
.testimonial {
  width: 80%;
  margin: auto;
}
</style>
