<template>
  <v-row>
    <v-col>
      Logging You In
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "processing",
  middleware({$auth, redirect}) {
    if ($auth.isLoggedIn) {
      redirect('dashboard')
    }
  }
}
</script>

<style scoped>

</style>
