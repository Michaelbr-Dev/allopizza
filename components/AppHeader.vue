<template>
  <v-app-bar :elevation="0" color="black" class="pa-3">
    <template #prepend>
      <a href="/">
        <v-img
          class="mr-1 ml-8"
          src="../public/assets/logo-tel.png"
          alt="Logo Allo Pizza"
          height="64"
          width="64"
          contain
        ></v-img>
      </a>
    </template>
    <v-app-bar-title>
      <div class="d-flex ga-5">
        <a href="/">
          <span class="website_title main align-self-center">ALLO PIZZA</span>
        </a>
        <div class="d-inline-flex flex-wrap">
          <span class="website_title sub d-none d-lg-block">2 rue Jean Jaurès</span>
          <span class="website_title sub d-none d-lg-block">59880 Saint-Saulve</span>
        </div>
      </div>
    </v-app-bar-title>

    <v-toolbar-items v-if="mdAndUp" class="align-center">
      <v-btn v-for="(item, i) in items" :key="i" :href="item.route" class="rounded-lg menu-btn">
        {{ item.title }}
      </v-btn>
      <a href="https://www.facebook.com/profile.php?id=100083018124674" target="_blank">
        <v-img
          class="mr-2"
          src="../public/assets/icone-fb.png"
          alt="Logo Facebook"
          height="32"
          width="32"
          contain
        ></v-img>
      </a>
    </v-toolbar-items>

    <v-toolbar-items v-if="smAndDown" class="align-right">
      <v-menu>
        <template #activator="{ props }">
          <v-btn icon="mdi-menu" variant="text" v-bind="props"></v-btn>
        </template>

        <v-list>
          <v-list-item v-for="(item, i) in items" :key="i" :href="item.route">
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
  { title: 'LES PIZZAS', route: '/' },
  { title: 'LES BOISSONS', route: '/boissons' },
  { title: 'LES DESSERTS', route: '/desserts' },
  { title: 'HISTORIQUE', route: '/historique' },
];
</script>

<style scoped>
.website_title {
  font-size: 30px;
  text-decoration: none;
}

.website_title.main {
  font-size: clamp(20px, 1.8vw, 30px);
  text-decoration: none;
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
a:link {
  text-decoration: none;
}
a:visited {
  text-decoration: none;
  color: white;
}
.menu-btn:hover {
  color: #cc0033;
}
</style>
