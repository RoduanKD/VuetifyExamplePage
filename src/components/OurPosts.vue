<template>
  <v-container
    id="posts"
    class="my-12"
  >
    <div class="text-h2 text-center">
      Our Posts
    </div>
    <v-row class="mt-6">
      <v-col
        v-for="(post, i) in posts"
        :key="i"
      >
        <v-card
          class="mx-auto"
          max-width="344"
        >
          <v-img
            :src="post.image"
            height="200px"
          />

          <v-card-title>
            {{ post.title }}
          </v-card-title>

          <v-card-subtitle>
            {{ post.subtitle }}
          </v-card-subtitle>

          <v-card-actions>
            <v-btn
              color="orange lighten-2"
              text
            >
              Explore
            </v-btn>

            <v-spacer />

            <v-btn
              icon
              @click="post.show = !post.show"
            >
              <v-icon>{{ post.show ? 'mdi-chevron-up' : 'mdi-chevron-down' }}</v-icon>
            </v-btn>
          </v-card-actions>

          <v-expand-transition>
            <div v-show="post.show">
              <v-divider />

              <v-card-text>
                {{ post.content }}
              </v-card-text>
            </div>
          </v-expand-transition>
        </v-card>
      </v-col>
    </v-row>
  </v-container>
</template>

<script>
export default {
  name: 'HelloWorld',

  data: () => ({
    posts: [
      {
        image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        title: 'Top western road trips',
        subtitle: '1,000 miles of wonder',
        content: "I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.",
        show: false,
      },
      {
        image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        title: 'Top western road trips',
        subtitle: '1,000 miles of wonder',
        content: "I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.",
        show: false,
      },
      {
        image: 'https://cdn.vuetifyjs.com/images/cards/sunshine.jpg',
        title: 'Top western road trips',
        subtitle: '1,000 miles of wonder',
        content: "I'm a thing. But, like most politicians, he promised more than he could deliver. You won't have time for sleeping, soldier, not with all the bed making you'll be doing. Then we'll go with that data file! Hey, you add a one and two zeros to that or we walk! You're going to do his laundry? I've got to find a way to escape.",
        show: false,
      },
    ],
  }),
}
</script>
