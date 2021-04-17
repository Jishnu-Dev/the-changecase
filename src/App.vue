<template>
  <img class="intro-img" alt="Vue logo" src="./assets/intro-img.svg">
  <HelloWorld msg="The Changecase By Jishnu Raj"/>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'

export default {
  name: 'App',
  components: {
    HelloWorld
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
.intro-img {
  width: 25vw !important;
  height: auto;
}
@media (max-width: 768px){
  .intro-img {
    width: 80vw !important;
    height: auto;
  }
}
</style>
