<template>
    <div>
        <!--播放器-->
        <div class="play-src">
            播放地址:
            <textarea type="text" placeholder="视频地址" v-model="videoSrc"></textarea>
        </div>
        <div style="width: 600px;margin: auto">
            <com-video></com-video>
        </div>
    </div>
</template>

<script>
    import ComVideo from '../../../components/video/video'

    export default {
        name: 'video-play',
        data () {
            return {
                videoSrc: 'http://musicdata.baidu.com/data2/video/567290761/ba857497bf5a3ad503c0fedd1aeb58c0/567290761.mp4'
            }
        },
        components: {
            ComVideo,
        }
    }
</script>

<style lang="scss" rel="stylesheet/scss" scoped>

</style>