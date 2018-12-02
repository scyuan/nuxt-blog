<template>
  <div class="container">
    <my-header />
    <div class="content">
      <div class="content-left">
        
        <my-card class="mb12">左侧内容</my-card>
      </div>
      <div class="content-right">
        <my-card class="mb12">关于我</my-card>
        <my-card class="mb12">搜索热门</my-card>
        <my-card class="mb12">
          <div slot="header">日期，标签</div>
        </my-card>
      </div>
    </div>
  </div>
</template>

<script>
import myHeader from '../components/myheader'
import myCard from '../components/myCard'
export default {
  components: {
    myHeader,myCard
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
</style>
