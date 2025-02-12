<template>
  <div>
    <HeroContainer :image="image" />
    <v-sheet class="text-center">
      <p class="h2 ma-3 pa-3 text-center ma-auto max-width-90%">
        Quelle est l'origine de la « pizza » ?
      </p>
      <p class="w-80 mx-auto my-4 d-md-none">
        D'origine d'Amérique du Sud, où la tomate était déjà cultivée, sa composition actuelle est
        d'origine italienne, plus précisément Napolitaine (Napoli = Naples). Le mot « pizza » est
        italien et introduit en France au XIXème siècle seulement alors qu'en Italie, ce terme était
        déjà utilisé depuis plus de dix siècles. Désormais omniprésente dans l'assiette des
        habitants des « quatre coins de la terre », la pizza est aujourd'hui un plat incontournable
        pour petits et grands.
      </p>
      <p class="w-75 mx-auto my-4 d-none d-md-block">
        D'origine d'Amérique du Sud, où la tomate était déjà cultivée, sa composition actuelle est
        d'origine italienne, plus précisément Napolitaine (Napoli = Naples). Le mot « pizza » est
        italien et introduit en France au XIXème siècle seulement alors qu'en Italie, ce terme était
        déjà utilisé depuis plus de dix siècles. Désormais omniprésente dans l'assiette des
        habitants des « quatre coins de la terre », la pizza est aujourd'hui un plat incontournable
        pour petits et grands.
      </p>
      <v-sheet class="gmap mx-auto">
        <iframe
          title="Naples"
          src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d2589207.6232230114!2d12.690664737992869!3d40.915379642260525!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x133b084f6a6c7e99%3A0x3df52cc13b78191d!2sNaples%2C+Italie!5e0!3m2!1sfr!2sfr!4v1563198517163!5m2!1sfr!2sfr"
          width="100%"
          height="100%"
          style="border: 0; aspect-ratio: 16/9"
          allowfullscreen=""
          loading="lazy"
          referrerpolicy="no-referrer-when-downgrade"
        ></iframe>
      </v-sheet>
    </v-sheet>
  </div>
</template>

<script setup>
import image from '../public/assets/photos/hero-historique.jpeg';
</script>

<style scoped>
.h2 {
  font-size: clamp(1rem, 1.8vw, 2rem);
  font-weight: bold;
}
.gmap {
  max-width: 700px;
  height: 100%;
  padding-bottom: 16px;
}
</style>
