<template>
  <v-app >
    <SideBar/>
    <v-main>
      <v-container fluid class="px-0">
        <nuxt/>
      </v-container>
    </v-main>
    <Footer/>
  </v-app>
</template>

<script>
import Footer from "~/components/Globals/Footer";
import SideBar from "~/components/Globals/SideBar";
export default {
name: "internal",
  components: {SideBar, Footer}
}
</script>

<style scoped>

</style>
