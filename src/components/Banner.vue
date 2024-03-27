<script setup>
  import { ref } from 'vue';

  const title = ref("Title");
  const description = ref("Description");
  const src = ref("https://cdn.vuetifyjs.com/images/cards/docks.jpg");
</script>

<template>
  <v-card
    class="banner-wrapper"
  >
  <v-img :src="src">
  </v-img>
    <template v-slot:title>
      This is a title
    </template>

    <v-card-text>
      This is content
    </v-card-text>
  </v-card>
</template>
<style>
.banner-wrapper {
  overflow: hidden;
  img {
    object-fit: fill;
    transition: all 0.2s ease-in;
    transform: scale(1.0);
    &:hover {
      transform: scale(1.1);
    }
  }
}
</style>