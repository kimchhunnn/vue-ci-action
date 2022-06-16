<template>
  <img alt="Vue logo" src="./assets/logo.png">
  <h3>{{ name }}</h3>
  <HelloWorld msg="Welcome to Your Vue.js App From Develop"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import {reactive, toRefs} from 'vue'

export default {
  name: 'App',
  components: {
    HelloWorld
  },
  setup() {
    const state = reactive({
      name: process.env.VUE_APP_NAME
    })

    return {
      ...toRefs(state)
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
