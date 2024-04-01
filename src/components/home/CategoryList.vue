<script setup>
import { ref } from 'vue';

const props = defineProps({
  title: String,
  categories: Array
});
 
</script>

<template>
  <v-container class="ma-0 pa-0 max-w-full" fluid>
    <v-row>
      <v-col md="6">
        <span class="text-h4">Featured Categories</span>
      </v-col>
      <v-col class="flex justify-end" md="6">
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
      <v-col cols="12" sm="6" md="4" lg="4" v-for="(category, index) in categories">
        <v-card>
          <v-card-title>{{ category.name }}</v-card-title>
        </v-card>
      </v-col>
    </v-row>
	</v-container>
</template>