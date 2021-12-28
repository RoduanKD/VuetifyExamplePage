<template>
  <v-container
    id="users"
    class="my-12"
  >
    <div class="text-h2 text-center">
      Our Users
    </div>
    <v-row>
      <v-col cols="12">
        <v-data-table
          :headers="headers"
          :items="items"
          :items-per-page="5"
          class="elevation-1"
        >
          <template #[`item.website`]="{ item }">
            <v-btn
              text
              :href="`http://${item.website}`"
              target="_blank"
            >
              {{ item.website }}
            </v-btn>
          </template>
        </v-data-table>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  data: () => ({
    headers: [
      {
        text: 'Name',
        value: 'name',
      },
      {
        text: 'Email',
        value: 'email',
      },
      {
        text: 'Phone',
        value: 'phone',
      },
      {
        text: 'ًُUser Webiste',
        value: 'website',
      },
    ],
    items: [],
  }),

  mounted () {
    const self = this
    this.axios.get('https://jsonplaceholder.typicode.com/users').then((res) => {
      self.items = res.data
    })
  },
}
</script>

<style>

</style>
