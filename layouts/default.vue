<template>
  <v-app >
    <NavBar/>
    <v-main>
      <v-container fluid class="px-0">
        <nuxt/>
      </v-container>
    </v-main>
    <Footer/>
  </v-app>
</template>

<script>
import Footer from '~/components/Globals/Footer'
import NavBar from "~/components/Globals/NavBar";
export default {
  components: {NavBar, Footer}
}
</script>

<style>
html {
  font-family: 'Poppins', 'sans-serif';
}
</style>
