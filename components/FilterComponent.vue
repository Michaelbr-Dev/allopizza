<template>
  <v-sheet class="bg-transparent">
    <v-row class="my-2 py-2 w-100 flex-wrap justify-center">
      <v-btn
        class="filter-btn rounded-xl"
        :class="{ selected: selectedCategory === 'all' }"
        variant="tonal"
        @click="selectCategory('all')"
      >
        Tout
      </v-btn>
      <v-btn
        v-for="category in uniqueCategories"
        :key="category"
        class="filter-btn rounded-xl"
        :class="{ selected: selectedCategory === category }"
        variant="tonal"
        @click="selectCategory(category)"
      >
        {{ category }}
      </v-btn>
    </v-row>
  </v-sheet>
</template>

<script setup>
import { ref, computed } from 'vue';

const props = defineProps({
  products: { type: Array, required: true },
});

const emit = defineEmits(['updateCategory']);

const selectedCategory = ref('all');

const uniqueCategories = computed(() => {
  const categories = props.products.map((product) => product.category);
  return [...new Set(categories)];
});

const selectCategory = (category) => {
  selectedCategory.value = category;
  emit('updateCategory', category);
};
</script>

<style scoped>
.filter-btn {
  border: solid 1px #444;
  margin: 5px;
}
.filter-btn:hover {
  background-color: #cc0033;
  border: solid 1px #cc0033;
  color: white;
}
.filter-btn.selected {
  background-color: #cc0033;
  border: solid 1px #cc0033;
  color: white;
}
</style>
