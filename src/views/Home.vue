<script lang="ts" setup>
</script>

<template>
	<v-container class="px-4" fluid>
		<v-row class="max-w-screen-2xl mx-auto w-full">
			<v-col sm="8" cols="12">
				<v-card
					class="mx-auto"
				>
					<v-carousel
						height="400"
						show-arrows="hover"
						cycle
						hide-delimiter-background
					>
						<v-carousel-item src="https://cdn.vuetifyjs.com/images/cards/docks.jpg" cover>
						</v-carousel-item>
					</v-carousel>
				</v-card>
			</v-col> 
			<v-col sm="4">
				<v-card
					class="mx-auto"
					prepend-icon="mdi-home"
				>
					<template v-slot:title>
						This is a title
					</template>

					<v-card-text>
						This is content
					</v-card-text>
				</v-card>
			</v-col> 
		</v-row>
	</v-container>
</template>
  