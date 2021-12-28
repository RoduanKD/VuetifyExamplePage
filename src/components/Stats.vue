<template>
  <v-container
    id="stats"
    class="my-12"
  >
    <v-row>
      <v-col cols="12">
        <div class="text-h2 text-center">
          Check the numbers
        </div>
      </v-col>
      <v-col
        v-for="(stat, i) in stats"
        :key="i"
        cols="4"
      >
        <v-sheet
          :color="stat.color"
          class="pa-5"
        >
          <div class="text-h1 text-center">
            <v-icon
              color="white"
              class="text-h1"
            >
              {{ stat.icon }}
            </v-icon>
          </div>
          <div class="text-h2 text-center white--text">
            {{ stat.title }}
          </div>
          <div class="subheading text-h5 text-center white--text">
            {{ stat.subtitle }}
          </div>
        </v-sheet>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    stats: [
      {
        color: 'primary',
        icon: 'mdi-account',
        title: '1M',
        subtitle: 'Users',
      },
      {
        color: 'success',
        icon: 'mdi-star',
        title: '5K',
        subtitle: 'Rating',
      },
      {
        color: 'primary',
        icon: 'mdi-account',
        title: '1M',
        subtitle: 'Users',
      },
    ],
  }),
}
</script>

<style>

</style>
