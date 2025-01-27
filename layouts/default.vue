<template>
  <v-layout
    class="rounded rounded-md"
    style="min-height: 100vh; display: flex; flex-direction: column"
  >
    <app-header />
    <v-main style="flex: 1">
      <slot />
    </v-main>
    <AppFooter />
  </v-layout>
</template>
