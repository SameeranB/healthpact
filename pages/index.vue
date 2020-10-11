<template>
  <v-row justify="center" align="center">
    <v-col cols="12">
      <v-row id="landing" >
        <v-col>
          <v-row id="heroImage" style="background-color: #FFECCC" class="mx-0 px-0">
            <v-col cols="6" style="height: 60vh" class="d-flex align-center justify-center">
              <v-img
                height="500"
                width="auto"
                contain
              :src="require('~/static/landing/fitness_app.svg')"
              ></v-img>
            </v-col>
            <v-col cols="6" class="d-flex align-center justify-center">
              <v-container class="d-flex flex-column align-center justify-center px-15">
                <span class="text-center text-h4 primary--text">You Don't Have To Tread This Path Alone</span>
                <v-divider></v-divider>
                <span class="text-center text-h6   my-15 px-10">Most of us are not able to complete our journey towards health because we lack self motivation. We're here to tell you that you do not have to do this alone. </span>
              </v-container>
            </v-col>
          </v-row>
          <v-row id="register_button" style="height: 20vh" class="d-flex align-center justify-center">
            <v-col class="d-flex flex-column align-center justify-center " cols="12">

              <v-btn
              v-if="$auth.loggedIn"
              color="secondary"
              @click="$router.push('dashboard')"
              >
                Open Dashboard
              </v-btn>

              <v-btn
              color="secondary"
              @click="$router.push('authentication')"
              v-else
              >
                Register Now
              </v-btn>
              <span class="text-center text-caption">It's Free. Forever.</span>
            </v-col>
          </v-row>
        </v-col>
      </v-row>
    </v-col>
  </v-row>
</template>

<script>
export default {

}
</script>
