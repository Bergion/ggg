<script setup>
import { ref } from 'vue';
import Banner from "@/components/home/Banner.vue";

const props = defineProps({
  products: Array
});

const banner = ref({
  title: "BODY PARTS",
  subtitle: "Wearing the best",
  src: "https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/rev_home3.png",
  btnText: "Shop now",
  btnPath: "/"
}); 

</script>
<template>
  <v-container class="ma-0 pa-0 max-w-full" fluid>
    <v-row>
      <v-col cols="12" md="6">
        <span class="text-3xl font-bold">Best Seller</span>
      </v-col>
    </v-row>
    <v-row>
      <v-col cols="12" md="4">
        <Banner 
          class="mb-8" 
          :title="banner.title"
          :subtitle="banner.subtitle"
          :src="banner.src"
          :btnText="banner.btnText"
          :btnPath="banner.btnPath"
          height="600"
        />
      </v-col>
      <v-col cols="12" md="8">
        <v-row>
          <v-col v-for="(product, index) in products"
            :key="index"
            cols="12" xs="12" sm="6" md="4">
            <v-card class="banner-wrapper w-full h-full" 
              image="https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/h3_category-1.jpeg"
              rounded="0"
              elevation="1"
            >
              <v-card-title class="px-6 py-4">
                <span class="text-sm">{{ product.categoryName }}</span>
                <v-spacer></v-spacer>
                <span class="font-bold">{{ product.name }}</span>
              </v-card-title>
              <v-card-actions class="px-6 pb-4">
                <v-btn
                  class="mb-2 bg-grey"
                  elevation="2"
                  rounded="0"
                >
                  <span class="text-xs font-semibold">Add to cart</span>
                </v-btn>
            </v-card-actions>
            </v-card>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
	</v-container>
</template>