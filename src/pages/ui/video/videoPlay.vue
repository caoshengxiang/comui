<template>
    <div>
        <!--播放器-->
        <div class="play-src">
            播放地址:
            <textarea cols="50" rows="3" type="text" placeholder="视频地址" v-model="videoSrc"></textarea>
            <button @click="OPlayHandle">切换播放源地址</button>
        </div>
        <div style="width: 600px;height: 400px;margin: auto">
            <com-video :src="videoSrc" :changeSrc="OPlayD"></com-video>
        </div>
    </div>
</template>

<script>
    import ComVideo from '../../../components/video/video'

    export default {
        name: 'video-play',
        data () {
            return {
                videoSrc: 'http://musicdata.baidu.com/data2/video/567290761/ba857497bf5a3ad503c0fedd1aeb58c0/567290761.mp4',
                OPlayD: false,
            }
        },
        components: {
            ComVideo,
        },
        methods: {
            OPlayHandle () {
                this.OPlayD = true
                setTimeout(()=> {
                    this.OPlayD = false
                }, 1)
            }
        }
    }
</script>

<style lang="scss" rel="stylesheet/scss" scoped>
.play-src{
    margin: 40px auto;
    text-align: center;
}
</style>