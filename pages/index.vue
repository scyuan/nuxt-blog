<template>
  <div class="container">
    <my-header />
    <div class="content">
      <div class="content-left">
        <my-card class="mb12" nopadding>
          <div slot="header">
            <menu-bar :activeIndex='index'>
              <menu-bar-item><span @click="changeCatalog(1)">热门</span></menu-bar-item>
              <menu-bar-item><span @click="changeCatalog(2)">分类1</span></menu-bar-item>
              <menu-bar-item><span @click="changeCatalog(3)">分类2</span></menu-bar-item>
            </menu-bar>
          </div>
          <div class="article" v-for="(item,index) in article" :key='index'>
            <img :src="item.img" style="height:100%;width:auto" alt="">
            <div class="article-content">
              <p class="a-title">{{ item.title }}</p>
              <p class="a-desc">{{ item.desc }}</p>
              <p class="a-info">
                
              </p>
            </div>
          </div>
        </my-card>
      </div>
      <div class="content-right">
        <my-card class="mb12">
          <div slot="header">关于我</div>
          <p>文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字</p>
        </my-card>
        <my-card class="mb12">
          <p>文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字</p>
        </my-card>

        <my-card class="mb12">
          <div slot="header">日期，标签</div>
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
</style>

