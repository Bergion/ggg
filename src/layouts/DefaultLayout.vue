<script lang="ts" setup>
  import Navbar from "@/components/navigation/Navbar.vue";
  import Footer from "@/components/navigation/Footer.vue";

</script>
<template>
  <v-app>
    <Navbar/>
		<!-- <SubNavbar/> -->
    <RouterView/>
    <Footer/>
  </v-app>
</template>