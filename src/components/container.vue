<template>
	<div>
		<h1>Dex Editor</h1>

		<aside><h1>Current Dex {{ count }}/10</h1>
		<ul id="example-1">
		  <li v-for="item in dex" :key="item.variantId">
			<h1><img v-bind:src="item.img"> {{ item.name }} x{{ item.quant }} </h1> 
		  </li>
		</ul>
		<p v-html='deck'></p></aside> 
		  <product name="Ghoul" type="Undead" atk =3 cost = 2 img = 'https://i.pinimg.com/originals/2a/99/a8/2a99a878e17b7527ea1f72b7730c6be9.gif' v-on:myEvent="handleClickInParent" v-on:myEventRm="handleClickInParentRm"></product>
		  
			<product name="Bunny" type="Cute" atk =32 cost = 23 img = 'https://media.tenor.com/images/875cc94bcbebef6efa10833a548e37ff/tenor.gif' v-on:myEvent="handleClickInParent" v-on:myEventRm="handleClickInParentRm"></product>

			<product name="Isabelle" type="Dogo" atk =0 cost = 0 img = 'https://66.media.tumblr.com/1268380c804aee668bcbb3b318d1a31b/tumblr_pg4gx02la91uwy5jno1_400.gifv' v-on:myEvent="handleClickInParent" v-on:myEventRm="handleClickInParentRm"></product>
	</div> 
</template>

<script>
	import product from '@/components/product.vue'
	export default {
	  name: 'container',
	  props: {
	  
	  },
		data() {
		return {
	  count: 0,
		  deck: "",
		  present: false,
		  
		  dex: [],
		}
	  },
		methods: {
		  handleClickInParentRm: function(name) {
				  for (var key in this.dex) { 
					this.present = false;
					var obj = this.dex[key];
					if (name === obj.name && obj.quant != 0){                

					  this.dex[key].quant -= 1
					  this.count -= 1;
					  if (obj.quant === 0){
						this.dex.splice(key, 1);
					  }
					
				  }
					
				  }
				 

	},
		  handleClickInParent: function(name, img) {
			this.present = false;
			if (this.count < 10) {   //Search          
			  for (var key in this.dex) {    
				  var obj = this.dex[key];
							if (name == obj.name){                

								this.dex[key].quant += 1
								this.present = true;
								this.count += 1;
								

							}
					
				  }
				  if (this.present == false){
					this.dex.push({ name: name, img: img,   quant: 1 });
					this.count += 1;
				  } ;
				   this.present = 0;
					
				  }; 

	}
		
		},
	  components: {
		product
	  }
	}
</script>
<style scoped></style>