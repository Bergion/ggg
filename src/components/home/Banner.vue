<script lang="ts" setup>
const props = defineProps({
  title: String,
  subtitle: String,
  src: String,
  btnText: String,
  btnPath: String,
  height: String,
  minHeight: String,
  elevation: Number
});

</script>

<template>
  <v-card class="banner-wrapper w-full h-full" 
    :min-height="minHeight"
    :height="height"
    :image="src"
    :elevation="elevation">
    <div class="px-6 py-8 h-full">
      <div class="flex flex-col justify-space-between h-full">
        <div>
          <v-card-title>
            <span class="text-4xl font-bold">{{ title }}</span>
          </v-card-title>

          <v-card-subtitle>
            <span class="text-bases">{{ subtitle }}</span>
          </v-card-subtitle>
        </div>
        <v-card-actions>
          <v-btn
            class="mb-2 rounded bg-grey"
            size="x-large"
            width="160"
            elevation="4"
            :to="btnPath"
          >
            <span class="text-xs font-semibold">{{ btnText }}</span>
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
  }
}
</style>