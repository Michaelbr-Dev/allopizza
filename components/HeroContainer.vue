<template>
  <v-parallax
    :height="mdAndUp ? 800 : 400"
    :src="props.image"
    class="responsive-image"
  ></v-parallax>
</template>

<script setup>
import { useDisplay } from 'vuetify';

const { mdAndUp } = useDisplay();

const props = defineProps({
  image: { String, Required: true },
});
</script>

<style scoped>
.responsive-image {
  width: 100%;
  height: auto;
}
</style>
