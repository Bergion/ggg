<script setup>
import { ref } from 'vue';
import { useDisplay } from 'vuetify';

const props = defineProps({
  title: String,
  categories: Array
});

const { name } = useDisplay();
</script>

<template>
  <v-container class="ma-0 pa-0 max-w-full" fluid>
    <v-row>
      <v-col cols="12" md="6">
        <span class="text-3xl font-bold">Featured Categories</span>
      </v-col>
      <v-col class="flex" :class="{'justify-end': name !== 'sm'}" cols="12" md="6">
        <v-btn class="mb-2 bg-grey"
          width="190"
          rounded="0"
          height="50"
          elevation="4">
          All categories
        </v-btn>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" sm="6" md="4" v-for="(category, index) in categories">
        <router-link to="/">
          <v-card class="banner-wrapper w-full h-full" 
            image="https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/h3_category-1.jpeg"
            rounded="0"
            elevation="1"
          >
            <v-card-title class="px-6 py-4">
              <span class="font-bold">{{ category.name }}</span>
            </v-card-title>
            <v-card-actions class="px-6 pb-4">
              <v-btn
                class="mb-2 bg-grey"
                elevation="2"
                rounded="0"
              >
                <span class="text-xs font-semibold">More</span>
              </v-btn>
          </v-card-actions>
          </v-card>
        </router-link>
      </v-col>
    </v-row>
	</v-container>
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