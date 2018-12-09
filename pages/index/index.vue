<template>
  <my-card class="mb12" nopadding>
    <div slot="header">
        <menu-bar :activeIndex='index'>
            <menu-bar-item><span @click="changeCatalog(1)">热门</span></menu-bar-item>
            <menu-bar-item><span @click="changeCatalog(2)">分类1</span></menu-bar-item>
            <menu-bar-item><span @click="changeCatalog(3)">分类2</span></menu-bar-item>
        </menu-bar>
    </div>
    <div class="article" v-for="(item,index) in article" :key='index' @click="$router.push({path:'/article/'})">
        <span class="article-tag">原创</span>
        <img :src="item.img" style="height:100%;width:auto" alt="">
        <div class="article-content">
            <p class="a-title">{{ item.title }}</p>
            <p class="a-desc">{{ item.desc }}</p>
            <p class="a-info">
                <span><i class="icon">&#xe603;</i>分类分类</span>
                <span><i class="icon">&#xe675;</i>2018年12月09日</span>
            </p>
        </div>
    </div>
</my-card>
</template>

<script>
import myHeader from '../../components/myheader'
import myCard from '../../components/myCard'
import menuBar from '../../components/menuBar'
import menuBarItem from '../../components/menuBarItem'
export default {
  transition:'page',
  components: {
    myHeader,myCard,menuBar,menuBarItem
  },
  data(){
    return{
      index:1,
      article:[
        {
          from:'原创',
          img:'https://p2.bahamut.com.tw/B/2KU/14/0001430614.JPG',
          title:'文字文字文字文字文字文字文字文字文字',
          desc:'文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字'
        },
        {
          from:'原创',
          img:'https://p2.bahamut.com.tw/B/2KU/14/0001430614.JPG',
          title:'文字文字文字文字文字文字文字文字文字',
          desc:'文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字'
        }
      ]
    }
  },
  methods:{
    changeCatalog(index){
      this.index=index;
    }
  }
}
</script>
<style>
@font-face {
  font-family: 'iconfont';  /* project id 957738 */
  src: url('//at.alicdn.com/t/font_957738_wot7bdwoc6m.eot');
  src: url('//at.alicdn.com/t/font_957738_wot7bdwoc6m.eot?#iefix') format('embedded-opentype'),
  url('//at.alicdn.com/t/font_957738_wot7bdwoc6m.woff') format('woff'),
  url('//at.alicdn.com/t/font_957738_wot7bdwoc6m.ttf') format('truetype'),
  url('//at.alicdn.com/t/font_957738_wot7bdwoc6m.svg#iconfont') format('svg');
}
.icon{
  font-family: 'iconfont';
  font-style: normal;
}
</style>

<style scoped>

.container {
  min-height: 100vh;
  display: flex;
  justify-content: center;
  text-align: center;
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
.mb12{
  margin-bottom: 12px;
}
.article{
  height: 120px;
  cursor: pointer;
  padding: 15px;
  display: flex;
  color: #333;
  position: relative;
  overflow: hidden;
}
.article:not(:last-child){
  border-bottom: 1px solid rgba(178,186,194,.15);
}
.article:hover{
  background: #fcfcfc;
}
.article-content{
  flex: 1;
  padding-left: 15px;
  font-size: 14px;
}
.a-title{
  font-weight: bold;
}
.a-desc{
  font-size: 13px;
  color: #999;
}
.article-tag{
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
.a-info{
  position: absolute;
  bottom: 15px;
  color: #999;
}
.a-info span{
  margin-right: 10px;
}
.a-info span i{
  margin-right: 2px;
}
</style>

