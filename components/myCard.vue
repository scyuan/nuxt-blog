<template>
    <div class="my-card">
        <div class="my-card-header" v-if="$slots.header || header">
            <slot name='header'></slot>
        </div>
        <div class="my-card-body">
            <slot></slot>
        </div>
    </div>
</template>
<script>
export default {
    props:{
        header:{}
    }
}
</script>
<style scoped>
.my-card{
    border-radius: 2px;
    text-align: left;
}
.my-card-header,.my-card-body{
    text-align: left;
    background: #fff;
    box-shadow: 0px 1px 2px 0px rgba(0, 0, 0, 0.05);
    
}
.my-card-header{
    border-bottom: 1px solid hsla(0,0%,59%,.1);
    padding: 10px 15px;
}
.my-card-body{
    padding: 15px;
}
</style>

