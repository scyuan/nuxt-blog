<template>
  <div id='article'>
    <my-card>
      <div
        slot="header"
        class="article-header"
      >
        <p class="back"><span @click="$router.back()"><i class="icon">&#xe60e;</i>返回</span></p>
        <h3 class="a-t">文字文字文字文字</h3>
        <p class="a-info">
          <span><i class="icon">&#xe603;</i>分类分类</span>
          <span><i class="icon">&#xe675;</i>2018年12月09日</span>
        </p>
      </div>
      <div class="article-content">
        <p>Amazon 的使命是 “To be Earth’s most customer-centric company”，就像阿里巴巴「让天下没有难做的生意」一样，都是伟大的使命。无论是潜规则抑或明文规定，每一个技术团队都应该有自己的使命，且一定是以技术为第一位。

          一个业务驱动的部门里，平常聊的都是业务，周会里也在谈业务，周报里依然全是业务项目汇报，全TM是业务。说实话我反感这样的团队，这样的团队往往变得越来越业务，越来越忽视技术，变得很“稳”，特别是团队项目都是哪些老旧的、念旧失修的系统的时候，“稳”到做很多技术规划时，都需要先把背景、目标和收益翻来覆去捯饬清楚，成员的激情一点点被消磨殆尽，技术人员会妥协，渐渐地更偏向于业务，反正只要系统运行良好就行了。
        </p>

      </div>
      <div class="article-info">
        <p>发布时间：2018-12-22 21:34:55</p>
        <p>更新时间：2018-12-22 21:35:05</p>
        <p>版权申明：版权声明：自由转载-署名-非商业性使用</p>
      </div>
    </my-card>
  </div>
</template>
<script>
import myCard from '../../../../components/myCard'
export default {
  components: {
    myCard
  }
}
</script>
<style scoped>
.back {
  color: #333;
  cursor: pointer;
  margin-bottom: 10px;
}
.back span:hover {
  color: #409eff;
}
.article-content,
.article-header {
  color: #333;
}
.a-t,
.a-info {
  text-align: center;
}
.a-info {
  color: #999;
  font-size: 12px;
  margin-top: 10px;
}
.a-info span {
  margin-right: 10px;
}
.a-info span i {
  margin-right: 2px;
}
.article-info {
  margin-top: 8px;
  padding: 8px;
  line-height: 2;
  background-color: #eee;
  border-left: 4px solid #ccc;
  font-weight: 300;
}
.article-info p {
  font-size: 14px;
  line-height: 20px;
}
</style>

