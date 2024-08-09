<template>
  <v-app-bar :elevation="0" color="black" class="pa-3">
    <template #prepend>
      <v-img
        class="mr-1 ml-8"
        src="../assets/logo/logo-tel-1.png"
        height="64"
        width="64"
        contain
      ></v-img>
    </template>
    <v-app-bar-title>
      <div class="d-flex ga-5">
        <span class="website_title">ALLO PIZZA</span>
        <span class="website_title">2 rue Jean Jaurès 59880 Saint-Saulve</span>
      </div>
    </v-app-bar-title>
    <v-toolbar-items class="align-center">
      <v-btn variant="text" slim> Les Pizzas </v-btn>
      <v-btn variant="text" slim> Les boissons </v-btn>
      <v-btn variant="text" slim> Les Desserts </v-btn>
      <v-btn variant="text" slim> Historique </v-btn>
      <v-btn variant="text" slim> Les boissons </v-btn>
      <v-img class="mr-2" src="../assets/icons/icone-fb.png" height="32" width="32" contain></v-img>
    </v-toolbar-items>
  </v-app-bar>
</template>

<style scoped>
.website_title {
  font-size: 30px;
}

.menu_block {
  justify-content: end;
}
.v-toolbar .v-btn {
  font-weight: bold;
  font-size: 16px;
}
</style>
