<template>
    <div>
        <li><a href="">Home</a></li>
        <li><a>Support</a>
        <li><a>News</a></li>
        <Navigation></Navigation>
    </div>
</template>

<script>
import Navigation from '@/components/Navigation.vue'

export default {
  name: 'links',
  components: {
    Navigation
  },
  props: {
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div{
  display:inline;
}
</style>
