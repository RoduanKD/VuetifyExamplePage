<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark
    >
      <div class="d-flex align-center">
        <v-img
          alt="Vuetify Logo"
          class="shrink mr-2"
          contain
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-logo-dark.png"
          transition="scale-transition"
          width="40"
        />

        <v-img
          alt="Vuetify Name"
          class="shrink mt-1 hidden-sm-and-down"
          contain
          min-width="100"
          src="https://cdn.vuetifyjs.com/images/logos/vuetify-name-dark.png"
          width="100"
        />
      </div>

      <v-spacer />

      <v-btn
        text
        @click="$vuetify.goTo('#posts')"
      >
        Posts
      </v-btn>
      <v-btn
        text
        @click="$vuetify.goTo('#gallery')"
      >
        Gallery
      </v-btn>
      <v-btn
        text
        @click="$vuetify.goTo('#stats')"
      >
        Statistics
      </v-btn>
      <v-btn
        text
        @click="$vuetify.goTo('#users')"
      >
        Users
      </v-btn>
      <v-btn
        icon
        color="white"
        @click="$vuetify.theme.dark = !$vuetify.theme.dark"
      >
        <v-icon v-if="!$vuetify.theme.dark">
          mdi-weather-night
        </v-icon>
        <v-icon v-else>
          mdi-weather-sunny
        </v-icon>
      </v-btn>
    </v-app-bar>

    <v-main>
      <router-view />
    </v-main>
    <v-footer class="text-center">
      &copy; 2022
    </v-footer>
  </v-app>
</template>

<script>

export default {
  name: 'App',

  data: () => ({
    //
  }),
}
</script>
