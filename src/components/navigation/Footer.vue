<script setup>
import { ref } from 'vue';

const contactDetails = ref({
	"phone": "+380 99 999 99 99",
	"address": "вул.Володимирівська, 33 м. Київ, 01601",
	"telegram": "@zalupa"
});
</script>
<template>
	<v-footer class="max-w-screen-2xl mx-auto w-full">
		<v-row class="pt-10">
			<v-col cols="12" sm="6" md="3"> 
				<router-link class="" to="/">
        	<v-img src="src/assets/logo-black.svg" width="50%"></v-img>
      	</router-link>
				<div class="text-2xl mt-8">{{ contactDetails['phone'] }}</div>
				<div class="text-lg mt-6">{{ contactDetails['address'] }}</div>
				<div class="text-lg mt-6">{{ contactDetails['telegram'] }}</div>
				
			</v-col>
			<v-col cols="12" sm="6" md="3">
				<strong>Информация</strong>
			</v-col>
			<v-col cols="12" sm="6" md="3">
				
			</v-col>
			<v-col cols="12" sm="6" md="3">
				
			</v-col>
		</v-row>
	</v-footer>
</template>