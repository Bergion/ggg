<script setup>
const props = defineProps({
	categoryName: String,
	name: String,
	src: String,
	price: Number
})
</script>
<template>
	<v-hover v-slot="{ isHovering, props }">
		<v-card class="w-full h-full" 
			rounded="0"
			elevation="1"
			v-bind="props"
		>
			<v-img class="ma-4" src="https://i.ebayimg.com/images/g/jU4AAOSwMtVhDDF1/s-l1200.webp">
				<v-overlay
				:model-value="isHovering"
				class="align-center justify-center"
				scrim="#767676"
				contained
				>
					<v-btn rounded="sm" color="black" variant="flat" icon="mdi-eye-outline"></v-btn>
				</v-overlay>
			</v-img>
			<v-card-title class="px-6 py-4">
				<router-link class="hoverable-link" to="/">
					<span class="text-sm">{{ categoryName }}</span>
				</router-link>
				<v-spacer></v-spacer>
				<router-link class="hoverable-link" to="/">
					<span class="font-bold text-base">{{ name }}</span>
				</router-link>
			</v-card-title>
			<v-card-text class="px-6 pb-0">
				<span class="font-weight-bold text-body-1">₴{{ price }}</span>
			</v-card-text>
			<v-card-actions class="px-6 pb-4">
				<v-btn
					class="mb-2"
					:class="[isHovering ? 'bg-black' : 'bg-grey']"
					elevation="2"
					rounded="0"
					block
				>
					<span class="text-xs font-semibold">Add to cart</span>
				</v-btn>
			</v-card-actions>
		</v-card>
	</v-hover>
</template>
<style>
 .hoverable-link:hover {
		color: grey;
 }
</style>