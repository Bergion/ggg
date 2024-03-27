<script setup>
  import { ref } from 'vue';

  const title = ref("Title");
  const description = ref("Description");
  const src = ref("https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/h3_banner-1.jpeg");
</script>

<template>
  <v-card class="banner-wrapper w-full h-full min-h-[285px]" :image="src">
    <div class="px-6 py-8 h-full">
      <div class="flex flex-col justify-space-between h-full">
        <div>
          <v-card-title class="text-h5">
            Supermodel
          </v-card-title>

          <v-card-subtitle>Foster the People</v-card-subtitle>
        </div>
        <v-card-actions>
          <v-btn
            class="mb-2 rounded bg-grey"
            size="x-large"
            width="160"
            elevation="4"
          >
            <span class="text-xs font-semibold">Shop now</span>
          </v-btn>
        </v-card-actions>
      </div>
    </div>
  </v-card>
</template>
<style>
  .v-card__image {
    width: calc(100% + 50px);
  }
  .banner-wrapper {
    & img {
      object-fit: cover;
      transition-duration: 300ms;
    }
    &:hover img {
      transform: translateX(-50px);
      transition-duration: 300ms;
      /* transform: translateX(-50px); */
    }
  }
</style>