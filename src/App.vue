<template>
  <v-app>
    <v-app-bar
      app
      color="primary"
      dark>
    </v-app-bar>

    <v-content>
          
    <div id="home">

    <nav class="user">
      <Links></Links>
    </nav>
    <header>
      <h1>
        <img src="./assets/logo.png" alt="The delta dex logo">
      </h1>
    </header>
    <a id="download" href="https://github.com/DeltadexGame/Launcher/releases/tag/0.9.0">Download Now</a>
  </div>


    </v-content>
  </v-app>
</template>

<script>
import Links from './components/Links';

export default {
  name: 'App',

  components: {
    Links,
  },

  data: () => ({
    //
  }),
};
</script>


<style>
*{
  transition: all 0.4s ease 0s;
}

#home {
  background-image:url("https://live.staticflickr.com/2880/10688206825_dd5aa4d3a5_b.jpg");
  background-size: 100%;
}

header{
  background: rgba(200, 200, 200, 0.6);
}

header:active{
  padding:0%
}

header img{
  height:60%;
  width:50%;
  display: block;
  margin-left: auto;
  margin-right: auto;
}

nav {
  padding-top:1%;
  background: rgba(0,0,0,0.5);
}

body {
  margin:0px;
}

li p {
  display:inline;
  color: black !important;
  text-transform: uppercase;
  text-decoration: none;
  background: #ed3330;
  padding-left: 4%; padding-right: 4%; padding-top: 1%; padding-bottom: 1%;
  border-radius: 5px;
  border: none;
  transition: all 0.4s ease 0s;
  margin-right:1%;
}

li p:hover{
text-shadow: 0px 0px 6px rgba(255, 255, 255, 1);
-webkit-box-shadow: 0px 5px 40px -10px rgba(0,0,0,0.57);
-moz-box-shadow: 0px 5px 40px -10px rgba(0,0,0,0.57);
transition: all 0.4s ease 0s;
}

a {
  display:inline;
  color: #fff !important;
  text-transform: uppercase;
  text-decoration: none;
  background: #ed3330;
  padding-left: 4%; padding-right: 4%; padding-top: 1%; padding-bottom: 1%;
  border-radius: 5px;
  border: none;
  transition: all 0.4s ease 0s;
  margin-right:1%;
}

li {
  display:inline;
}

a:hover {
  text-shadow: 0px 0px 6px rgba(255, 255, 255, 1);
  -webkit-box-shadow: 0px 5px 40px -10px rgba(0,0,0,0.57);
  -moz-box-shadow: 0px 5px 40px -10px rgba(0,0,0,0.57);
  transition: all 0.4s ease 0s;
}

ul {
  list-style-type: none;
  margin: 0;
  padding: 0;
}

h1{
  margin:0%;
}

img {
  margin-left: auto;
  width: 5%;
  height: 5%;
}

figure {
display: inline;
margin-left: 45%
}

#download {
  margin-LEFT: auto;
  margin-right:auto;
  float:left;
}

#error {
  color: red;
}

#reg{
  display:inline;
}

.login{
  display:block;
  margin:1%
}

footer a{
  display:block;
  text-align: center;
  margin-top:1%;
  border:2px;
  border-color:black;
}

button{
  color: #ed3330 !important;
  text-transform: uppercase;
  text-decoration: none;
  background: #fff;
  padding: 20px; padding-top:10px; padding-bottom:10px;
  border-radius: 5px;
  display: inline-block;
  border: none;
  transition: all 0.4s ease 0s;
  margin:.5%;
}

button, li{
  cursor: pointer;
}

button:hover{
  text-shadow: 0px 0px 6px rgba(255, 255, 255, 1);
  -webkit-box-shadow: 0px 5px 40px -10px rgba(220,0,0,0.57);
  -moz-box-shadow: 0px 5px 40px -10px rgba(0,0,0,0.57);
  transition: all 0.4s ease 0s;
}

input[type=text], select, input[type=password] {
  width: 20%;
  padding: .5% 20px;
  margin: 8px 0;
  margin-left:1%;
  display: inline-block;
  border: 1px solid #ccc;
  border-radius: 4px;
  box-sizing: border-box;
}

input[type=submit], password {
  display:inline;
  width: 20%;
  background-color: #4CAF50;
  color: white;
  padding: 14px 20px;
  margin: 8px 0;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}

input[type=submit]:hover {
  background-color: #45a049;
}
</style>
