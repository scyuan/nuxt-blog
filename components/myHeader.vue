<template>
  <header>
    <div class="content">
      <ul class="menu">
        <li class="item logo">YUAN</li>
        <li class="item item_active">首页</li>
        <li class="item">XXXX</li>
        <li class="item">XXXX</li>
        <li class="item">XXXX</li>
      </ul>
    </div>
    
  </header>
</template>

<script>
export default {}
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
  background: #ccc;
}
.item_active {
  color: #000;
}
.item_active::before {
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
}
</style>
