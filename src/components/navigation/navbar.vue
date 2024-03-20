<script setup>
import { ref } from 'vue';

const loading = ref(false);

</script>
<template>
  <div>
    <v-toolbar class="bg-black text-white" :height="120">
      <router-link class="flex align-center w-1/4 md:py-5 md:px-8" to="/">
        <v-img src="src/assets/logo-black.svg"></v-img>
      </router-link>
      <v-text-field
        class="p-10"
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
    <!-- <nav class="container">
      <div class="flex">
        <router-link to="/">
          Logo
        </router-link>
      </div>
    </nav> -->
  </div>
</template>