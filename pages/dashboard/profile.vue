<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-row align="center" justify="center">
        <v-col cols="5">
          <v-card class="d-flex mx-5">
            <v-card-title>
              <v-avatar height="150" width="150">
                <v-img height="150" contain :src="$auth.user.picture"></v-img>
              </v-avatar>
            </v-card-title>
            <v-row class="d-flex flex-column">
              <v-card-title>{{ $auth.user.given_name }} <br/> {{ $auth.user.family_name }}</v-card-title>
              <v-card-text>My Bio</v-card-text>
            </v-row>
          </v-card>
        </v-col>
        <v-spacer></v-spacer>
        <v-col cols="2">
          <v-btn
            color="red"
          >
            Delete Account
          </v-btn>
        </v-col>
      </v-row>
      <v-row>
        <v-col cols="12">
          <v-card class="mx-5">
            <v-row>
              <v-col>
                <v-card-text
                  v-for="detail in userDetails"
                >
                  {{ detail.title }}: {{ detail.value }}
                </v-card-text>

              </v-col>
              <v-spacer></v-spacer>
              <v-card-actions>
                <v-btn
                 c
                ></v-btn>
              </v-card-actions>
            </v-row>
          </v-card>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>

<script>
export default {
  name: "profile",
  layout: "internal",
  data() {
    return {
      userDetails: [
        {
          title: "Name",
          value: this.$auth.user.given_name
        },
        {
          title: "Email",
          value: this.$auth.user.email
        },
        {
          title: "Gender",
          value: "Male"
        },
        {
          title: "Name",
          value: 21
        }
      ]
    }
  }
}
</script>

<style scoped>

</style>
