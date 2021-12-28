<template>
  <v-parallax
    dark
    src="https://cdn.vuetifyjs.com/images/backgrounds/vbanner.jpg"
  >
    <v-row
      align="center"
      justify="center"
      class="align-content-center"
    >
      <v-col
        class="text-center"
        cols="12"
      >
        <h1 class="text-h1 font-weight-thin mb-4">
          Vuetify
        </h1>
        <h4 class="subheading">
          Build your application today!
        </h4>
      </v-col>
      <v-col
        class="text-center"
        col="12"
      >
        <v-btn color="primary">
          Get started
        </v-btn>
      </v-col>
    </v-row>
  </v-parallax>
</template>

<script>
export default {
  name: 'HelloWorld',

  data: () => ({}),
}
</script>
