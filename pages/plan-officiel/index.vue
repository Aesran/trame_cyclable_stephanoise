<template>
  <div class="w-full">
    <img
      src=https://raw.githubusercontent.com/Aesran/voies_stephanoises/refs/heads/main/assets/0-Schema-structurant-SEM.png
      class="object-contain w-full h-screen"
      :alt="`plan officiel des ${getRevName()}`"
    >
  </div>
</template>

<script setup lang="ts">
const { getRevName } = useConfig();

const description = `Découvrez le plan officiel des ${getRevName()}, le futur réseau vélo Stéphanois`;
const COVER_IMAGE_URL = 'https://raw.githubusercontent.com/Aesran/voies_stephanoises/refs/heads/main/assets/0-logo-carte.png';

useHead({
  title: `Plan des ${getRevName()}`,
  meta: [
    // description
    { hid: 'description', name: 'description', content: description },
    { hid: 'og:description', property: 'og:description', content: description },
    { hid: 'twitter:description', name: 'twitter:description', content: description },
    // cover image
    { hid: 'og:image', property: 'og:image', content: COVER_IMAGE_URL },
    { hid: 'twitter:image', name: 'twitter:image', content: COVER_IMAGE_URL }
  ]
});
</script>
