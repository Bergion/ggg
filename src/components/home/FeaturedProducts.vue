<script setup>
import { ref, computed } from 'vue';
import Banner from "@/components/home/Banner.vue";
import ProductCard from "@/components/ProductCard.vue";

const props = defineProps({
  products: Array
});

const banner = ref({
  title: "BODY PARTS",
  subtitle: "Wearing the best",
  src: "https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/h3_banner-5.jpeg",
  btnText: "Shop now",
  btnPath: "/"
}); 

const featuredProducts = computed(() => {
  props.products.slice(0, 6);
})
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
          elevation="0"
          height="970"
        />
      </v-col>
      <v-col cols="12" md="8">
        <v-row>
          <v-col v-for="(product, index) in products"
            :key="index"
            cols="12" xs="12" sm="6" md="4">
            {{ console.log(product.categoryName) }}
            <ProductCard
              :category-name="product.categoryName"
              :name="product.name"/>
          </v-col>
        </v-row>
      </v-col>
    </v-row>
	</v-container>
</template>