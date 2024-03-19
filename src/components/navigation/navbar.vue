<script setup>
const height = "15rem";
</script>
<template>
  <div>
    <v-toolbar class="bg-white text-black" :height="height">
      <router-link class="flex align-center w-1/4" to="/">
        <v-img src="src/assets/logo-black.svg"></v-img>
      </router-link>
      <v-toolbar-title>Title</v-toolbar-title>
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