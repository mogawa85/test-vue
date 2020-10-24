<template>
<div id="current-id">
  <h1>Hi Veronica! Welcome to the viva-LA-vue Workshop!</h1>
  <div> I am a developer named {{ firstName }}{{ firstName }}. Watch me as I code in Vue.js! </div>

  <p>
    My First Name is: <input type="text" v-model="firstName">
    <br>
    My Last Name is: <input type="text" v-model="lastName">
  </p>
  <div>
    <button @click="doSomething(!myBoolean)"> Toggle Me </button> This is our boolean: {{ myBoolean }}
  </div>
  <!-- <div>
    <img v-if="myBoolean" src="http://www.fillster.com/images/pictures/10p.jpg">
  </div> -->
  <div style="display:flex; align-items: center; justify-content: center;">
    <bouncing-ball ballcolor="red"></bouncing-ball>
    <bouncing-ball ballcolor="rgb(255,255,0)"></bouncing-ball>
    <bouncing-ball></bouncing-ball>
    <bouncing-ball ballcolor="#ADFF2F"></bouncing-ball>
    <bouncing-ball ballcolor="cornflowerblue"></bouncing-ball>
  </div>
</div>
</template>

<script>
import BouncingBall from "./components/BouncingBall.vue"
export default {
  data() {
    return {
      firstName: 'Miki',
      lastName: 'Ogawa',
      myBoolean: true,
    }
  },
  methods: {
    doSomething(boolean) {
      this.myBoolean = boolean
    }
  },
  components: {
    BouncingBall
  }
}
</script>

<style>
#current-id{
  font-family: Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #42b883;
  margin-top: 60px;
}
  </style>
