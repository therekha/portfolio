<template>
  <HelloWorld 
  class="center"
  />
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
@import url('https://fonts.googleapis.com/css2?family=Space+Grotesk&display=swap');

#app {
  min-height: 98vh;
  font-family: 'Space Grotesk', Michroma, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;

  opacity: 1;
  background-image: radial-gradient(var(--rosepink) 0.45px, var(--inkblue) 0.45px);
  background-size: 9px 9px;

  display:flex;
  justify-content:center;
  align-items:center;
}
.center{
  background-color: var(--inkblue);
  padding: 5vh 10vh;
  border-style: solid;
  border-color: var(--oldyellow);
}

</style>
