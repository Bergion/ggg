<script setup>
import { ref } from 'vue';

const items = ref([
  { title: "Главная"},
  { title: "Оплата"},
  { title: "Доставка"},
  { title: "Гарантия"},
  { title: "Контакты"},
]);

const categories = ref([
  { title: "Генераторы"},
])
</script>
<template>
  <v-toolbar class="bg-grey-darken-4 text-white">
    <div class="max-w-screen-2xl mx-auto w-full px-8">
      <v-menu>
        <template v-slot:activator="{ props }">
          <v-btn rounded="0" width="15%" class="bg-grey" height="64" flat prepend-icon="mdi-menu" v-bind="props">Категории</v-btn>
        </template>
        <v-list>
          <v-list-item
            v-for="(item, index) in categories"
            :key="index"
          >
            <v-btn class="h-full" density="default">
              {{ item.title }}
            </v-btn>
          </v-list-item>
        </v-list>
      </v-menu>
      <v-btn 
        v-for="(item, index) in items"
        :key="index"
        height="64"
        flat 
      > 
        {{ item.title }}
      </v-btn>
    </div>
  </v-toolbar>
</template>