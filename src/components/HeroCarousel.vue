<script lang="ts" setup>
import { computed } from 'vue';
const propd = defineProps({
  slides: Array
});

</script>

<template>
  <v-sheet
    elevation="3"
    class="mx-auto"
  >
    <v-carousel
      direction="vertical"
      :show-arrows="false"
      hide-delimiter-background
      continuous
      height="600"
    >
      <v-carousel-item v-for="(slide, index) in slides" 
        :key="index" 
        position="100% 150px" 
        :src="slide.src">
          <div class="relative d-flex flex-col justify-space-around w-1/2 ml-[10%] h-full">
            <div class="text-5xl mb-10 font-bold">
              {{ slide.text }}
            </div>
            <v-btn
            class="mb-2 rounded bg-grey"
            size="x-large"
            width="160"
            elevation="4"
          >
            <span class="text-xs font-semibold">{{ slide.btnText }}</span>
          </v-btn>
        </div>
      </v-carousel-item>
    </v-carousel>
  </v-sheet>

</template>

<style>
.v-carousel__controls {
  color: black
}

.v-carousel-item .v-img {
  height: calc(100%);
}
</style>