<script setup>
import { ref } from 'vue';

const items = ref([
  { title: "Категория 1"},
  { title: "Категория 2"},
])
</script>
<template>
  <v-toolbar class="bg-grey-darken-4 text-white">
    <div class="max-w-screen-2xl mx-auto w-full px-8">
      <v-menu open-on-hover>
        <template v-slot:activator="{ props }">
          <v-btn height="100" flat prepend-icon="mdi-menu" v-bind="props">Категории</v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="(item, index) in items"
            :key="index"
          >
            <v-btn class="h-full" density="default">
              {{ item.title }}
            </v-btn>
          </v-list-item>
        </v-list>
      </v-menu>
    </div>
  </v-toolbar>
</template>