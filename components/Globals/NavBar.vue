<template>
  <v-card tile dark>
    <v-app-bar
      fixed
      color="secondary"
      app
      elevate-on-scroll
    >

      <v-app-bar-nav-icon class="hidden-sm-and-up"></v-app-bar-nav-icon>

      <v-toolbar-title @click="$router.push('/')" style="cursor: pointer">
        <v-avatar
          tile
        >
          <v-img
            :src="require('~/static/logo.svg')"
            contain
          ></v-img>
        </v-avatar>
        <span class="mx-3 text-h6">HealthPact</span>
      </v-toolbar-title>

      <v-spacer></v-spacer>
      <template
        v-if="$auth.loggedIn"
      >
        <v-btn
          outlined
          class="mx-2"
          @click="$router.push('dashboard')"
        >
          Open Dashboard
        </v-btn>

        <v-btn
          class="mx-2 "
          color="red"
          @click="$auth.logout()"

        >
          Logout
        </v-btn>

      </template>
      <template v-else>
        <v-btn
          outlined
          class="mx-2"
          @click="$router.push('authentication')"
        >
          Login
        </v-btn>
        <v-btn
          outlined
          class="mx-2"
          @click="$router.push('authentication')"
        >
          Register
        </v-btn>
      </template>
    </v-app-bar>
  </v-card>
</template>

<script>
export default {
  name: "NavBar"
}
</script>

<style scoped>

</style>
