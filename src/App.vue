<template>
  <h1>Ninja Reaction Timer </h1>
  <button @click="start"  :disabled="isPlaying">Play</button>
  <Block v-if="isPlaying" :delay="delay"/>
</template>

<script>
import Block from "./components/Block.vue"
export default {

  name: 'App',
  data() {
    return {
      isPlaying: false,
      delay: null,
    }
  },
  components: {Block},
  methods: {
    start() {
      this.delay = 2000 + Math.random() * 5000
      this.isPlaying = true
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
 button{
  background: grey;
  padding: 8px 4px;
 }
</style>
