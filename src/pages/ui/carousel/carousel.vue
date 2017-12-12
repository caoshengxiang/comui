<template>
  <div style="">
    <h1 class="h1">轮播图</h1>

    <!--test 轮播组件-->
    <div style="margin-left: 200px;margin-bottom: 50px;">
      <h3>默认</h3>
      <div style="width: 800px; height: 400px">
        <carousel :images="images" @imgClick="imgI"></carousel>
      </div>
    </div>
    <div style="margin-left: 200px;margin-bottom: 50px;">
      <h3>左右按钮在两侧,不显示列表</h3>
      <div style="width: 800px; height: 400px">
        <carousel :images="images" :interval="2000" btnSide="outside" :listDisplay="false" @imgClick="imgI"></carousel>
      </div>
    </div>
    <div style="margin-left: 200px;margin-bottom: 50px;">
      <h3>列表在下方,轮播周期１S,无左右按钮</h3>
      <div style="width: 800px; height: 400px">
        <carousel :images="images" listSide="outside" :interval="1000" :btnDisplay="false" @imgClick="imgI"></carousel>
      </div>
    </div>
    <div style="margin-left: 200px;margin-bottom: 50px;">
      <h3>默认</h3>
      <div style="width: 800px; height: 400px">
        <carousel :images="images" :interval="2000" @imgClick="imgI"></carousel>
      </div>
    </div>
    <div style="margin-left: 200px;margin-bottom: 50px;">
      <h3>列表在左侧</h3>
      <div style="width: 800px; height: 400px">
        <carousel :images="images" :interval="2000" listPosition="left" :btnDisplay="false" @imgClick="imgI"></carousel>
      </div>
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
      },
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
    },
  }
</script>
<style lang="scss" rel="stylesheet/scss" scoped>
  @import '../../../styles/common';
</style>