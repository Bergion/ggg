<script lang="ts" setup>
import { ref } from 'vue'
import Banner from "@/components/home/Banner.vue";
import HeroCarousel from "@/components/home/HeroCarousel.vue";
import CategoryList from "@/components/home/CategoryList.vue";
import FeaturedProducts from "@/components/home/FeaturedProducts.vue";

const slides = ref([
	{
		text: "Aftermarket Turbocharger Specialist",
		src: "https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/rev_home3.png",
		btnText: "Discover now",
	},
	{
		text: "Aftermarket Turbocharger Specialist",
		src: "https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/rev_home1.png",
		btnText: "Discover now",
	}
]);

const banners = ref([
	{
		title: "Title",
		subtitle: "Subtitle",
		src: "https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/h3_banner-1.jpeg",
		btnText: "Shop now",
		btnPath: "/"
	},
	{
		title: "Title",
		subtitle: "Subtitle",
		src: "https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/h3_banner-1.jpeg",
		btnText: "Shop now",
		btnPath: "/"
	}
]);

const featuredProducts = ref(Array(6).fill(
	{
		categoryName: 'Starters',
		name: "Starter",
		src: "https://demothemedh.b-cdn.net/rbpazt/wp-content/uploads/2021/08/h3_banner-1.jpeg",
		price: 1000
	})
);
</script>

<template>
	<v-container class="py-8 home-container" fluid>
		<v-row class="max-w-screen-2xl mx-auto w-full">
			<v-col md="8" cols="12">
				<HeroCarousel :slides="slides"/>
			</v-col> 
			<v-col lg="4">
				<div class="flex flex-col h-full">
					<Banner
						v-for="(banner, index) in banners"
						:key="index" 
						class="mb-8" 
						:title="banner.title"
						:subtitle="banner.subtitle"
						:src="banner.src"
						:btnText="banner.btnText"
						:btnPath="banner.btnPath"
						height="285"
					/>
				</div>
			</v-col> 
		</v-row>
		<v-row class="max-w-screen-2xl mx-auto w-full">
			<v-col cols="12">
				<CategoryList :categories="[{name: 'Tires'}, {name: 'Engines'}, {name: 'Starters'}, {name: 'Generators'}]"/>
			</v-col>
		</v-row>
		<v-row class="max-w-screen-2xl mx-auto w-full">
			<v-col cols="12">
				<FeaturedProducts :products="featuredProducts"/>
			</v-col>
		</v-row>
	</v-container>
</template>

