<template>
  <v-row style="height: 84vh">
    <v-col style="height: 100%" class="d-flex align-center justify-center">
      <v-row class="d-flex align-center justify-center">
        <v-col cols="4" class="d-flex flex-column">
          <span class="text-right text-h6">
            Why We Only Provide Google OAuth
          </span>
          <span class="text-right text-subtitle-2 my-4" style="color: grey">
            Our system works by collecting health data from your Google account and working our magic on that data. In order for us to successfully provide you our services, we need OAuth access to your Google Account.
          </span>
        </v-col>
        <v-divider vertical></v-divider>
        <v-col cols="4">
          <v-card
            class="d-flex flex-column align-center justify-center mx-15"
            hover
            ripple
            color="accent"
          >
            <v-card-title><v-icon x-large>mdi-google</v-icon></v-card-title>
            <v-card-text class="text-center text-h6">Continue With Google</v-card-text>
          </v-card>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "authentication"
}
</script>

<style scoped>

</style>
