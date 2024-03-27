<script lang="ts" setup>
  import Navbar from "@/components/navigation/Navbar.vue";
  import SubNavbar from "@/components/navigation/Subnavbar.vue";

</script>
<template>
  <v-app>
    <Navbar/>
		<SubNavbar/>
    <RouterView/>
  </v-app>
</template>