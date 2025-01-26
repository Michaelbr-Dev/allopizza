<template>
  <div class="testimonial">
    <v-row justify="center">
      <v-col v-for="product in props.products" :key="product.id" lg="3">
        <v-sheet class="rounded-lg testimonial-cell">
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
  width: 90%;
  margin: auto;
  margin-bottom: 20px;
}

.testimonial-cell {
  min-width: 300px;
  display: flex;
  align-items: center;
  justify-content: center;
}
</style>
