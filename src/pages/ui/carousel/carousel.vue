<template>
  <div>
<h1 class="h1">轮播图</h1>

    <!--test 轮播组件-->
    <div style="width: 800px; height: 400px">
      <carousel :images="images" :interval="2000" @imgClick="imgI"></carousel>
    </div>
  </div>
</template>
<script>
  import carousel from '../../../components/carousel/carousel.vue'
  import timg1 from '../../../assets/test/c1.jpg'
  import timg2 from '../../../assets/test/c2.jpg'
  import timg3 from '../../../assets/test/c3.jpg'
  import timg4 from '../../../assets/test/c4.jpg'
  import timg5 from '../../../assets/test/c5.jpg'
  export default {
    name: '',
    props: {},
    data () {
      return {
          images: [
              'http://mpic.tiankong.com/403/871/40387119bd4f65ec01f93fc3b3bae8b1/640.jpg',
              'http://mpic.tiankong.com/b71/8e1/b718e16820c85d7f3356734a82d81e0f/17-0113.jpg',
              'http://mpic.tiankong.com/999/0ec/9990ecbd5f67f413b987934fa73221ab/640.jpg',
              'http://mpic.tiankong.com/e48/4d2/e484d234d68c6d9b891ff639efbe7a29/640.jpg',
              'http://mpic.tiankong.com/cf5/844/cf58442c1d45ecfddbf36d4ac760e21b/640.jpg',
          ],
        img: [timg1, timg2, timg3, timg4, timg5],
      }
    },
    computed: {},
    methods: {
      imgI (n) {
        alert(n)
      }
    },
    components: {
      carousel,
    },
    beforeCreate () {
    },
    created () {
    },
    beforeMount () {
    },
    mounted () {
    },
    beforeUpdate () {
    },
    updated () {
    },
    beforeDestroy () {
    },
    destroyed () {
    }
  }
</script>
<style lang="scss" rel="stylesheet/scss" scoped>
  @import '../../../styles/common';
</style>