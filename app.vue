<template>
  <NuxtLayout :name="layout">
    <NuxtPage />
  </NuxtLayout>
</template>

<script setup>
const layout = 'default';

useSeoMeta({
  title: 'Allopizza Saint-Saulve',
  ogTitle: 'Allopizza Saint-Saulve',
  description: 'Retrouvez le goût des saveurs avec Allopizza Saint-Saulve !',
  ogDescription: 'Retrouvez le goût des saveurs avec Allopizza Saint-Saulve !',
});
</script>
