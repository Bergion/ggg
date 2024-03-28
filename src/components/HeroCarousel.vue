<script lang="ts" setup>
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
      <v-carousel-item position="100% 150px" src="https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/rev_home3.png">
          <div class="relative d-flex flex-col w-1/2 ustify-space-between h-full">
            <div class="text-h2">
              Text
            </div>
            <v-btn
            class="mb-2 rounded bg-grey"
            size="x-large"
            width="160"
            elevation="4"
          >
            <span class="text-xs font-semibold">Discover Now</span>
          </v-btn>
        </div>
      </v-carousel-item>
      <v-carousel-item position="100% 150px" src="https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/rev_home1.png"/>
    </v-carousel>
  </v-sheet>

</template>

<style>
  .v-carousel-item .v-img {
  height: calc(100% + 150px);
}
</style>