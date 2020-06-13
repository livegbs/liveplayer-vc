<template>
  <div id="app">
    <LivePlayer videoUrl="video.mp4"/>
    <HelloWorld msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
import HelloWorld from './components/HelloWorld.vue'
import LivePlayer from '@liveqing/liveplayer'

export default {
  name: 'App',
  components: {
    HelloWorld,
    LivePlayer
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
