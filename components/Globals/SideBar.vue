<template>
  <v-navigation-drawer
    permanent
    width="auto"
    fixed
    app
  >
    <v-row
      class="fill-height"
      no-gutters
    >
      <v-navigation-drawer
        dark
        mini-variant
        mini-variant-width="56"
        permanent
        expand-on-hover
      >
        <v-list-item class="px-2">
          <v-list-item-avatar>
            <v-img :src="$auth.user.picture"></v-img>
          </v-list-item-avatar>
          <v-list-item-content>
            <v-list-item-title>{{ $auth.user.given_name }} {{$auth.user.family_name}}</v-list-item-title>
          </v-list-item-content>
        </v-list-item>
        <v-divider></v-divider>
        <v-list
          nav
        >
          <v-list-item
            v-for="item in miniBarItems"
            :key="item.title"
            @click="$router.push(item.link)"
          >
            <v-list-item-action>
              <v-icon>{{ item.icon }}</v-icon>
            </v-list-item-action>

            <v-list-item-content>
              <v-list-item-title>{{ item.title }}</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
          <v-list-item
          @click="$auth.logout()"
          >
            <v-list-item-action>
              <v-icon>mdi-logout</v-icon>
            </v-list-item-action>

            <v-list-item-content>
              <v-list-item-title>Logout</v-list-item-title>
            </v-list-item-content>
          </v-list-item>
        </v-list>
      </v-navigation-drawer>
      <v-list class="pr-5">
        <v-list-item>
          <v-list-item-title class="d-flex align-center justify-center text-h5">
            Bubble Productivity
          </v-list-item-title>
        </v-list-item>
        <v-divider></v-divider>
        <v-list-item
        v-for="item in sideBarItems"
        :key="item.title"
        link
        class="my-2"
        @click="$router.push(item.link)"
        >
          <v-list-item-icon><v-icon left>{{item.icon}}</v-icon></v-list-item-icon>
          <v-list-item-title>{{item.title}}</v-list-item-title>
        </v-list-item>
      </v-list>
    </v-row>
  </v-navigation-drawer>
</template>

<script>
export default {
  name: "SideBar",
  data() {
    return {
      miniBarItems: [
        {
          title: "Home",
          icon: "mdi-home",
          link: "/"
        },
        {
          title: "Settings",
          icon: "mdi-cog",
          link: "dashboard/settings"
        },
      ],
      sideBarItems: [
        {
          title: "Group Name",
          link: "dashboard/group",
          icon: "mdi-account-group"
        },
        {
          title: "My Goals",
          link: "dashboard/goals",
          icon: "mdi-bullseye-arrow"
        },
        {
          title: "My Statistics",
          link: "dashboard/statistics",
          icon: "mdi-chart-box"
        },
        {
          title: "My Profile",
          link: "dashboard/profile",
          icon: "mdi-account"
        },
      ]
    }
  },
  methods: {
    logoutUser() {
      this.$auth.logout()
    },

  }
}
</script>

<style scoped>

</style>
