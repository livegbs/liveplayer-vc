<template>
<div class="hello">

    <div style="width:512px;height:300px;margin:auto">
        <LivePlayer videoUrl="video.mp4" />
    </div>
    <div style="width:512px;height:300px;margin:auto" class="palyer2">
        <!-- 用 http://localhost:8080 访问demo可以播放下面的flv -->
        <LivePlayer  @snapOutside="snapOutside" ref="player2" videoUrl="http://localhost:8080/video.flv" live />
    </div>

    <h1>{{ msg }}</h1>
    <h3>相关说明</h3>
    <ul>
        <li><a href="https://www.liveqing.com/docs/manuals/LivePlayer.html#%E5%B1%9E%E6%80%A7-property" target="_blank" rel="noopener">属性(Property)</a></li>
        <li><a href="https://www.liveqing.com/docs/manuals/LivePlayer.html#%E6%96%B9%E6%B3%95-medthod" target="_blank" rel="noopener">方法(Medthod)</a></li>
        <li><a href="https://www.liveqing.com/docs/manuals/LivePlayer.html#%E4%BA%8B%E4%BB%B6-event" target="_blank" rel="noopener">事件(Event)</a></li>
    </ul>

    <h3>方法调用示例</h3>
    <ul>
        <li><a @click="pause" rel="noopener">暂停</a></li>
        <li><a @click="play" rel="noopener">播放</a></li>
        <li><a @click="snap" rel="noopener">截图数据</a></li>
    </ul>
    <br/>
    <br/>
</div>
</template>

<script>
import LivePlayer from '@liveqing/liveplayer'
export default {
    name: 'LivePlayerDemo',
    components: {
        LivePlayer
    },
    props: {
        msg: String
    },
    methods: {
        pause: function () {
            this.$refs.player2.pause();
        },
        play: function () {
            this.$refs.player2.play();
        },
        snap: function () {
            this.$refs.player2.snap();
        },
        snapOutside: function (snapData) {
            alert(snapData)
        }
    }
}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->

<style scoped>
h3 {
    margin: 40px 0 0;
}

ul {
    list-style-type: none;
    padding: 0;
}

li {
    display: inline-block;
    margin: 0 10px;
    cursor: pointer;
}

a {
    color: #42b983;
}
</style>
