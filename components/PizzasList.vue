<template>
  <v-container class="mx-auto" max-width="100%">
    <v-row>
      <v-col v-for="product in props.products" :key="product.id" cols="12" sm="6" md="4" lg="3">
        <v-card class="rounded-lg card">
          <a v-if="product.link" :href="product.link" target="_blank">
            <v-img
              :src="assetPath + product.img"
              class="responsive-image align-end"
              height="auto"
              cover
            >
            </v-img>
            <v-card-actions class="flex-column justify-center">
              <v-card-title class="text-white mx-auto">
                {{ product.name + (product.price ? ' - ' + product.price : '') }}
              </v-card-title>
              <v-card-subtitle class="mx-auto mt-n2 text-white">
                {{ product.subName }}
              </v-card-subtitle>
            </v-card-actions>
          </a>
          <div v-else>
            <a :href="`/${product.id}`">
              <v-img
                :src="assetPath + product.img"
                class="responsive-image align-end"
                height="auto"
                cover
              >
              </v-img>
              <v-card-actions class="flex-column justify-center v-card--density-compact">
                <v-card-title class="text-white mx-auto">
                  {{ product.name + (product.price ? ' - ' + product.price : '') }}
                </v-card-title>
                <v-card-subtitle class="mx-auto mt-n2 text-white">
                  {{ product.subName }}
                </v-card-subtitle>
              </v-card-actions>
            </a>
          </div>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script setup>
const assetPath = 'assets/pizzas-miniatures/';
const props = defineProps({
  products: { type: Array, required: true },
});
</script>

<style scoped>
.card {
  border: solid 1px #444;
}
.responsive-image {
  width: 100%;
  height: auto;
}
.a {
  text-decoration: none;
}
a:link {
  text-decoration: none;
}
</style>
