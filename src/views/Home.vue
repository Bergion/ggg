<script lang="ts" setup>
	import Banner from "@/components/Banner.vue";
	import HeroCarousel from "@/components/HeroCarousel.vue";

</script>

<template>
	<v-container class="px-0 py-8" fluid>
		<v-row class="max-w-screen-2xl mx-auto w-full px-4 h-50">
			<v-col md="8" cols="12">
				<HeroCarousel/>
			</v-col> 
			<v-col lg="4">
				<div class="flex flex-col h-full">
					<Banner 
						class="mb-8" 
						title="Title"
						subtitle="Subtitle"
						src="https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/h3_banner-1.jpeg"
						btnText="Shop now"
						btnPath="/"
					/>
					<Banner 
						class="mb-8" 
						title="Title"
						subtitle="Subtitle"
						src="https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/h3_banner-1.jpeg"
						btnText="Shop now"
					/>
				</div>
			</v-col> 
		</v-row>
	</v-container>
</template>

