<template>
    <span class="menu-bar-item">
        <span><slot></slot></span>
    </span>
</template>
<script>
export default {
    
}
</script>
<style scoped>
.menu-bar-item{
    cursor: pointer;
}
.menu-bar-item_active{
    color: #000;
}
</style>

