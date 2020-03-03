<template>
    <div>
        <li><a href="">Home</a></li>
        <li><a>Support</a>
        <li><a>News</a></li>

           <v-btn icon class="align-self-start" size="28">
        <v-icon>mdi-arrow-right-thick</v-icon>
      </v-btn>

      
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
