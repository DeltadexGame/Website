<template>
<div>
    <div class="user">
        <!--Logged In-->
        <div v-if="logged">

            <li><p>Weclome:- {{UserName}} </p></li>
            <div class="login">
                <li>
                    <button v-on:click="logout">Log Out</button>
                </li>
                <li>Win/Loss: {{ kd }}</li>
                  <li><button v-on:click="won">Win!</button></li>
                  <li><button v-on:click="lost">Lose!</button></li>
            </div>
			<container></container>
        </div>

        <!--Logged Out-->
        <div v-else>
            <li>
              <a v-on:click="reg">{{ reglog }}</a>
            </li>
            <p id="error">{{ error }}</p>
            <div v-if="register">
                    <button v-on:click="login">Register</button>
                    <input type="password" name="Uname" v-model="UserName" placeholder="Username">
                    <input type="password" name="Pword" placeholder="Password">
                    <input type="text" name="Email" placeholder="Email">
            </div>
            <div v-else>
                    <button v-on:click="login">Login</button>
                    <input type="text" name="Uname" v-model="UserName" placeholder="Username">
                    <input type="password" name="Pword" placeholder="Password">
            </div>
      </div>
    </div>
</div>
</template>

<script>
/* eslint-disable */
import container from '@/components/container.vue'
export default {
  name: 'Navigation',
  props: {
    reglog: 'Register',
    show: true,
    wins: 0,
    losses: 0,
    UserName: '',
    register: false,
    logged: false,
    test: 0,
    inStock: true,
    variants: [],
    error: ''
  },
  methods: {
    logout () {
      this.logged = false
      this.wins = 0
      this.losses = 0

    },
    won () {
      this.wins += 1

    },
    lost () {
      this.losses += 1

    },
    reg () {
        this.error = ""
        this.register = !this.register
        if (this.reglog === 'Register'){
            this.reglog = 'Login'
        }
        else {
            this.reglog = 'Register'
        }
    },

    login () {
      if (this.UserName === '') {
          this.error = 'Please Enter a valid Username.'
      } else {
        this.logged = true
      }

    }
  },
  components: {
	container,
  },
  computed: {
    kd () {
      return this.wins + '/' + this.losses
    }
  }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
div{
  display:inline;
}
</style>
