<template>
  <v-row
    id="gallery"
    class="my-12"
  >
    <v-col cols="12">
      <div class="text-h2 text-center">
        Gallery
      </div>
    </v-col>
    <v-col
      v-for="i in 6"
      :key="i"
      cols="4"
    >
      <v-hover v-slot="{ hover }">
        <v-img src="https://picsum.photos/500">
          <v-overlay
            v-if="hover"
            absolute
            color="#036358"
          >
            <v-row
              justify="center"
              align="center"
              class="fill-height"
            >
              <div class="text-h5">
                This is a hover effect
              </div>
            </v-row>
          </v-overlay>
        </v-img>
      </v-hover>
    </v-col>
  </v-row>
</template>
