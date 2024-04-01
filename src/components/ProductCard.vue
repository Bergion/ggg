<script setup>
const props = defineProps({
	categoryName: String,
	name: String,
	src: String
})
</script>
<template>
  <v-card class="w-full h-full" 
		rounded="0"
		elevation="1"
	>
		<v-img src="https://i.ebayimg.com/images/g/jU4AAOSwMtVhDDF1/s-l1200.webp"></v-img>
		<v-card-title class="px-6 py-4">
			<span class="text-sm">{{ categoryName }}</span>
			<v-spacer></v-spacer>
			<span class="font-bold">{{ name }}</span>
		</v-card-title>
		<v-card-actions class="px-6 pb-4">
			<v-btn
				class="mb-2 bg-grey"
				elevation="2"
				rounded="0"
				block
			>
				<span class="text-xs font-semibold">Add to cart</span>
			</v-btn>
	</v-card-actions>
	</v-card>
</template>