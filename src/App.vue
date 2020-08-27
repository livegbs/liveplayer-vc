<template>
<div id="app">
    <LivePlayerDemo msg="LivePlayer.js H5直播点播播放器演示" />
</div>
</template>

<script>
import LivePlayerDemo from './components/LivePlayerDemo.vue'

export default {
    name: 'App',
    components: {
        LivePlayerDemo
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
