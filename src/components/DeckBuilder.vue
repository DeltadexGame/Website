<template>
<div class="product">
          <v-app id="inspire">
          <v-card max-width="200">
    <v-img
        class="blue--text align-end"
        height="100px"
        v-bind:src = 'img'
      ><v-card-title>{{ name }}</v-card-title>
      </v-img>

      <v-card-subtitle class="pb-0"> {{ type }} Type</v-card-subtitle>

      <v-card-text class="text--primary">
        <div>Attack: {{ atk }} Cost:{{ cost }}</div>

      </v-card-text>

      <v-card-actions>
        <v-btn
          color="orange"
          text
          @click="addToDeck"
        >
          Add
        </v-btn>

        <v-btn
          color="orange"
          text
@click="removeFromDeck"
        >
          Remove
        </v-btn>
      </v-card-actions>


    </v-card>
</v-card>
</v-app>
    </div>
</template>

<script>
export default {
  name: 'HelloWorld',
  props: {
       name: String,
    type: String,
    img: String,
    atk: String,
    cost: String,
  }
  data() {
    return {
        deck: "",
        cart: 0
    }
  },
    methods: {
      addToCart: function() {
          this.cart += 1
      },
     addToDeck: function() {
       this.$emit('myEvent', this.name, this.img);

     },
      removeFromDeck: function(){
        this.$emit('myEventRm', this.name);
      }
    }
}
</script>


<style scoped>

img{
  height: 1em;
}

aside{
  border-style: inset;
  background-color: 660000;
  left: 90%;
  position: fixed;
  top: 0;
  padding-bottom:100%;
}

.product{
  height:250px;
  width:200px;
}
</style>