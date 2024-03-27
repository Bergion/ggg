<script setup>
  import { ref } from 'vue';

  const title = ref("Title");
  const description = ref("Description");
  const src = ref("https://cdn.vuetifyjs.com/images/cards/docks.jpg");
</script>

<template>
  <v-card class="banner-wrapper w-full h-full" :image="src">
    <div class="d-flex flex-no-wrap justify-space-between px-6 py-8">
      <div>
        <v-card-title class="text-h5">
          Supermodel
        </v-card-title>

        <v-card-subtitle>Foster the People</v-card-subtitle>

        <v-card-actions>
          <v-btn
            class="ms-2"
            size="small"
            variant="outlined"
          >
            START RADIO
          </v-btn>
        </v-card-actions>
      </div>
    </div>
  </v-card>
</template>
<style>
  .banner-wrapper:hover .v-img {
    transition-duration: 300ms;
    transform: translateX(-50px);
  }
</style>