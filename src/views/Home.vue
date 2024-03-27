<script lang="ts" setup>
	import Banner from "@/components/Banner.vue";

</script>

<template>
	<v-container class="px-0 py-8" fluid>
		<v-row class="max-w-screen-2xl mx-auto w-full px-4 h-50">
			<v-col sm="8" cols="12">
				<v-card
					class="mx-auto"
				>
					<v-carousel
						show-arrows="hover"
						cycle
						hide-delimiter-background
						height="600"
					>
						<v-carousel-item src="https://cdn.vuetifyjs.com/images/cards/docks.jpg" cover>
						</v-carousel-item>
					</v-carousel>
				</v-card>
			</v-col> 
			<v-col sm="4">
				<div class="flex flex-col h-full">
					<Banner class="mb-8"/>
					<Banner/>
				</div>
			</v-col> 
		</v-row>
	</v-container>
</template>
  