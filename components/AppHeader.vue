<template>
  <v-app-bar :elevation="0" color="black" class="pa-3">
    <template #prepend>
      <v-img
        class="mr-1 ml-8"
        src="../public/assets/logo-tel.png"
        height="64"
        width="64"
        contain
      ></v-img>
    </template>
    <v-app-bar-title>
      <div class="d-flex ga-5">
        <span class="website_title main align-self-center">ALLO PIZZA</span>
        <div class="d-inline-flex flex-wrap">
          <span class="website_title sub d-none d-lg-block">2 rue Jean Jaurès</span>
          <span class="website_title sub d-none d-lg-block">59880 Saint-Saulve</span>
        </div>
      </div>
    </v-app-bar-title>

    <v-toolbar-items v-if="mdAndUp" class="align-center">
      <v-btn v-for="(item, i) in items" :key="i">{{ item.title }}</v-btn>
      <v-img
        class="mr-2"
        src="../public/assets/icone-fb.png"
        height="32"
        width="32"
        contain
      ></v-img>
    </v-toolbar-items>

    <v-toolbar-items v-if="smAndDown" class="align-right">
      <v-menu>
        <template #activator="{ props }">
          <v-btn icon="mdi-menu" variant="text" v-bind="props"></v-btn>
        </template>

        <v-list>
          <v-list-item v-for="(item, i) in items" :key="i">
            <v-list-item-title>{{ item.title }}</v-list-item-title>
          </v-list-item>
        </v-list>
      </v-menu>
    </v-toolbar-items>
  </v-app-bar>
</template>

<script setup>
import { useDisplay } from 'vuetify';

const { mdAndUp, smAndDown } = useDisplay();

const items = [
  { title: 'LES PIZZAS' },
  { title: 'LES BOISSONS' },
  { title: 'LES DESSERTS' },
  { title: 'HISTORIQUE' },
];
</script>

<style scoped>
.website_title {
  font-size: 30px;
}

.website_title.main {
  font-size: clamp(20px, 1.8vw, 30px);
}

.website_title.sub {
  font-size: clamp(20px, 1.8vw, 30px);
}

.menu_block {
  justify-content: end;
}

.v-toolbar .v-btn {
  font-weight: bold;
  font-size: clamp(14px, 1vw, 18px);
}
</style>
