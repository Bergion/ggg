<script setup>
import { ref } from 'vue';

const loading = ref(false);

</script>
<template>
  <div class="px-8 py-5">
    <div class="max-w-screen-2xl mx-auto">
      <v-toolbar class="bg-white text-black">
        <router-link class="w-1/5 px-5" to="/">
          <v-img src="src/assets/logo-black.svg"></v-img>
        </router-link>
        <v-text-field
          class="mx-10"
          append-inner-icon="mdi-magnify"
          density="compact"
          label="Пошук по VIN"
          variant="solo"
          hide-details
          single-line
          @click:append-inner="() => loading = !loading"
        ></v-text-field>
        <v-btn icon>
          <v-icon size="large">mdi-account</v-icon>
        </v-btn>
        <v-btn icon>
          <v-icon>mdi-cart</v-icon>
        </v-btn>
      </v-toolbar>
    </div>
  </div>
</template>