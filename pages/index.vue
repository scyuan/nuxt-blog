<template>
  <div class="container">
    <my-header />
    <div class="content">
      <div class="content-left">
        <nuxt-child></nuxt-child>
      </div>
      <div class="content-right">
        <!-- <my-card class="mb12">
          <div slot="header">关于我</div>
          <p>文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字</p>
        </my-card> -->
        <my-card class="mb12">
          <p>文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字</p>
        </my-card>

        <my-card class="mb12">
          <div slot="header">标签</div>
          <p>文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字</p>
        </my-card>
      </div>
    </div>
  </div>
</template>

<script>
import myHeader from '../components/myheader'
import myCard from '../components/myCard'
import menuBar from '../components/menuBar'
import menuBarItem from '../components/menuBarItem'
export default {
  transition: 'page',
  components: {
    myHeader,
    myCard,
    menuBar,
    menuBarItem
  },
  data() {
    return {
      index: 1,
      article: [
        {
          from: '原创',
          img: 'https://p2.bahamut.com.tw/B/2KU/14/0001430614.JPG',
          title: '文字文字文字文字文字文字文字文字文字',
          desc:
            '文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字'
        },
        {
          from: '原创',
          img: 'https://p2.bahamut.com.tw/B/2KU/14/0001430614.JPG',
          title: '文字文字文字文字文字文字文字文字文字',
          desc:
            '文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字'
        }
      ]
    }
  },
  methods: {
    changeCatalog(index) {
      this.index = index
    }
  }
}
</script>
<style>
@font-face {
  font-family: 'iconfont'; /* project id 957738 */
  src: url('//at.alicdn.com/t/font_957738_jotyubndexi.eot');
  src: url('//at.alicdn.com/t/font_957738_jotyubndexi.eot?#iefix')
      format('embedded-opentype'),
    url('//at.alicdn.com/t/font_957738_jotyubndexi.woff') format('woff'),
    url('//at.alicdn.com/t/font_957738_jotyubndexi.ttf') format('truetype'),
    url('//at.alicdn.com/t/font_957738_jotyubndexi.svg#iconfont') format('svg');
}
.icon {
  font-family: 'iconfont';
  font-style: normal;
}
</style>

<style scoped>
.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
}
.content {
  width: 913px;
  padding-top: 73px;
  display: flex;
  justify-content: space-between;
}
.content-left {
  width: 600px;
}
.content-right {
  width: 300px;
}
.mb12 {
  margin-bottom: 12px;
}
.article {
  height: 120px;
  cursor: pointer;
  padding: 15px;
  display: flex;
  color: #333;
  position: relative;
  overflow: hidden;
}
.article:not(:last-child) {
  border-bottom: 1px solid rgba(178, 186, 194, 0.15);
}
.article:hover {
  background: #fcfcfc;
}
.article-content {
  flex: 1;
  padding-left: 15px;
  font-size: 14px;
}
.a-title {
  font-weight: bold;
}
.a-desc {
  font-size: 13px;
  color: #999;
}
.article-tag {
  position: absolute;
  z-index: 1;
  right: -23px;
  top: -26px;
  font-size: 12px;
  background: red;
  color: #fff;
  padding: 30px 19px 2px 35px;
  transform: rotate(35deg);
}
.a-info {
  position: absolute;
  bottom: 15px;
  color: #999;
}
.a-info span {
  margin-right: 10px;
}
.a-info span i {
  margin-right: 2px;
}
</style>

