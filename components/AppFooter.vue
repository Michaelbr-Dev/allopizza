<template>
  <footer class="footer">
    <div class="container">
      <v-row justify="center" class="flex-wrap">
        <v-col lg="3">
          <v-sheet class="rounded-lg Footer-cell">
            <div justify="center">
              <h3 class="mt-3">Contact</h3>
              <p class="mt-2">
                Addresse: 2 Rue Jean-Jaures<br />
                59300 Saint-Saulve
              </p>
              <p class="mt-2">tél: 03 27 27 04 04</p>
              <div class="pt-3 d-flex flex-column align-center">
                <v-img
                  class="mr-2 rounded"
                  src="../public/assets/icone-fb.png"
                  height="32"
                  width="32"
                  contain
                ></v-img>
                <v-img
                  class="mr-2 mt-2"
                  src="public/assets/logo-tel.png"
                  height="150"
                  width="150"
                  contain
                ></v-img>
              </div>
            </div>
          </v-sheet>
        </v-col>
        <v-col lg="3">
          <v-sheet class="rounded-lg Footer-cell">
            <div justify="center" class="w-100">
              <h3 class="mt-3">Horaires</h3>
              <p class="mt-2">
                Du mardi au samedi <br />
                11h30 - 13h30 | 18h00 - 22h00
              </p>
              <p class="mt-2 font-weight-bold">Fermé le dimanche et le lundi</p>
              <div class="d-flex flex-row justify-space-evenly align-center flex-wrap my-3 w-100">
                <v-img
                  class="rounded-lg"
                  src="public/assets/paiements.jpg"
                  width="180px"
                  height="180px"
                  contain
                ></v-img>
                <v-img
                  class="rounded-lg"
                  src="public/assets/cbna.jpg"
                  width="215px"
                  height="159px"
                  contain
                ></v-img>
              </div>
            </div>
          </v-sheet>
        </v-col>
        <v-col lg="3">
          <v-sheet class="rounded-lg Footer-cell pa-2">
            <iframe
              title="Google Maps"
              src="https://www.google.com/maps/embed?pb=!1m18!1m12!1m3!1d1984.9626622866929!2d3.541230175521925!3d50.36666749339421!2m3!1f0!2f0!3f0!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x47c2edfa77f03ac3%3A0x270c91002fb3a53d!2s2%20Rue%20Jean%20jaures%2C%2059300%20Saint-Saulve!5e1!3m2!1sfr!2sfr!4v1737911151541!5m2!1sfr!2sfr"
              width="100%"
              height="100%"
              style="border: 0"
              allowfullscreen=""
              loading="lazy"
              referrerpolicy="no-referrer-when-downgrade"
            >
            </iframe>
          </v-sheet>
        </v-col>
      </v-row>
      <div class="mt-7">
        <p class="text-caption">Tous suppléments payants - Photos non contractuelles</p>
        <p class="text-caption">
          Pour votre santé, mangez au moins 5 fruits et légumes par jour :
          <NuxtLink to="http://www.mangerbouger.fr" target="_blank">Mangerbouger.fr</NuxtLink>
        </p>
        <p class="text-caption">
          « L’abus d’alcool est dangereux pour la santé. À consommer avec modération »
        </p>
        <p class="text-caption">
          &copy; Copyright 2019 Allo Pizza St Saulve - Tous droits réservés
        </p>
      </div>
    </div>
  </footer>
</template>

<script setup>
// You can add any necessary script logic here
</script>

<style scoped>
.footer {
  margin-top: 20px;
  background-color: #000;
  padding: 16px;
  text-align: center;
}
.Footer-cell {
  min-width: 290px;
  height: 100%;
  display: flex;
  align-items: start;
  justify-content: center;
}
</style>
