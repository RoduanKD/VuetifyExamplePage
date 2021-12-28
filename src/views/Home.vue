<template>
  <div>
    <hero />
    <our-posts />
    <gallery />
    <stats />
    <banner />
    <users />
  </div>
</template>

<script>
import Hero from '../components/Hero'
import OurPosts from '../components/OurPosts'
import Gallery from '../components/Gallery'
import Stats from '../components/Stats'
import Banner from '../components/Banner'
import Users from '../components/Users'

export default {
  name: 'Home',

  components: {
    Hero,
    OurPosts,
    Gallery,
    Stats,
    Banner,
    Users,
  },
}
</script>
