<script setup>
import { ref } from 'vue';

const loading = ref(false);

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
  <v-toolbar class="bg-white text-black" height="100%" >
    <v-container class="pa-0 h-full" fluid>
      <v-row class="max-w-screen-2xl mx-auto pt-3 px-3">
        <v-col class="my-1" sm="3">
          <router-link to="/">
            <v-img src="src/assets/logo-black.svg"></v-img>
          </router-link>
        </v-col>
        <v-col class="self-center" sm="8">
          <v-text-field
            class="mx-10"
            append-inner-icon="mdi-magnify"
            density="compact"
            label="Пошук по VIN"
            variant="solo"
            hide-details
            single-line
            @click:append-inner="() => loading = !loading"
          ></v-text-field>
        </v-col>
        <v-col class="flex self-center" sm="1">
          <v-btn icon>
            <v-icon size="large">mdi-account</v-icon>
          </v-btn>
          <v-btn icon>
            <v-icon>mdi-cart</v-icon>
          </v-btn>
        </v-col>
      </v-row>
      <v-row class="bg-grey-darken-4 text-white px-3">
        <v-col class="pt-0" cols="12">
          <div class="max-w-screen-2xl mx-auto w-full px-3">
            <v-menu>
              <template v-slot:activator="{ props }">
                <v-btn class="bg-grey" 
                  rounded="0" 
                  width="15%" 
                  height="64" 
                  prepend-icon="mdi-menu"
                  v-bind="props"
                  flat>Категории</v-btn>
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
        </v-col>
      </v-row>
    </v-container>
  </v-toolbar>
</template>