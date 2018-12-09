<template>
    <div id='article'>
        <p class="back"><span><i class="icon">&#xe60e;</i>返回</span></p>
        <my-card>
            <div slot="header" class="article-header">
                <h3 class="a-t">文字文字文字文字</h3>
                <p class="a-info">
                    <span><i class="icon">&#xe603;</i>分类分类</span>
                    <span><i class="icon">&#xe675;</i>2018年12月09日</span>
                </p>
            </div>
            <div class="article-content">
                <p>文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字
                    文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字
                    文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字
                    文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字
                    文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字
                    文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字
                    文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字
                    文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字文字
                </p>
            </div>
        </my-card>
    </div>
</template>
<script>
import myCard from '../../../../components/myCard'
export default {
    components:{
        myCard
    }
}
</script>
<style scoped>
.back{
    color: #333;
    cursor: pointer;
    margin-bottom: 10px;
}
.back:hover{
    color: blue;
}
.article-content,.article-header{
    color: #333;
}
.a-info{
  color: #999;
  font-size: 12px;
  margin-top: 10px;
}
.a-info span{
  margin-right: 10px;
}
.a-info span i{
  margin-right: 2px;
}
</style>

