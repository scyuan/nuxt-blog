<template>
  <header>
    <div class="content">
      <ul class="menu">
        <div
          class="bingo"
          ref='bingo'
        ></div>
        <li class="item logo">
          &lt;yuan /&gt;
        </li>
        <li
          :class="['item',curr_path=='/'?'item_active':'']"
          @click="page($event,'/')"
          ref='home'
        >首页</li>
        <li
          :class="['item',curr_path=='/archive'?'item_active':'']"
          @click="page($event,'/archive')"
          ref='archive'
        >归档</li>
        <li
          :class="['item',curr_path=='/about'?'item_active':'']"
          @click="page($event,'/about')"
          ref="about"
        >关于</li>

      </ul>
    </div>

  </header>
</template>

<script>
export default {
  data() {
    return {
      curr_path: '/'
    }
  },
  methods: {
    page(e, path) {
      this.curr_path = path
      const left = e.target.getBoundingClientRect().left
      const width = e.target.getBoundingClientRect().width
      this.$refs.bingo.style.left = `${left}px`
      this.$refs.bingo.style.width = `${width}px`
      this.$router.push({ path: path })
    }
  },
  mounted() {
    const path = this.$route.path
    var left = ''
    var width = ''
    switch (path) {
      case '/archive':
        left = this.$refs.archive.getBoundingClientRect().left
        width = this.$refs.archive.getBoundingClientRect().width

        break
      case '/about':
        left = this.$refs.about.getBoundingClientRect().left
        width = this.$refs.about.getBoundingClientRect().width
        break
      default:
        left = this.$refs.home.getBoundingClientRect().left
        width = this.$refs.home.getBoundingClientRect().width
        break
    }
    this.$refs.bingo.style.left = `${left}px`
    this.$refs.bingo.style.width = `${width}px`
  }
}
</script>

<style scoped>
header {
  position: fixed;
  height: 60px;
  width: 100%;
  top: 0;
  left: 0;
  background: #fff;
  display: flex;
  align-items: center;
  border-bottom: 1px solid #f1f1f1;
  color: #909090;
}
.content {
  width: 913px;
  margin: 0 auto;
}
.menu {
  line-height: 40px;
}
.item {
  float: left;
  margin-right: 30px;
  cursor: pointer;
  color: #555;
  position: relative;
}
.logo {
  width: 100px;
  height: 40px;
  color: #000;
  font-size: 20px;
}
.item_active {
  color: #000;
}
.bingo {
  position: fixed;
  height: 3px;
  background: #000;
  width: 0%;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
  top: 0;
  left: 0;
  box-shadow: 0px 1px 5px 1px rgba(0, 0, 0, 0.7);
  transition: all 0.3s;
}
/* .item_active::before {
  content: '';
  display: block;
  position: absolute;
  height: 3px;
  background: #000;
  width: 100%;
  border-bottom-right-radius: 2px;
  border-bottom-left-radius: 2px;
  top: -10px;
  box-shadow: 0px 1px 5px 1px rgba(0, 0, 0, 0.7);
} */
</style>
