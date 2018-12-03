<template>
    <div class="my-menu-bar">
        <slot></slot>
    </div>
</template>
<script>
export default {
    props:{
        activeIndex:{
            type:Number,
            default:1
        }
    },
    provide(){
        return{
            menuBar:this,
            setIndex:function(index){
                this.activeIndex = index;
            }
        }
    },
    methods:{
        active(){
            const items = this.$el.querySelectorAll('.menu-bar-item');
            items.forEach((element,index) => {
                element.setAttribute('class','menu-bar-item');
            });
            items[parseInt(this.activeIndex)-1].setAttribute('class','menu-bar-item menu-bar-item_active');
        }
    },
    watch:{
        'activeIndex':function(){
            this.active();
        }
    },
    mounted(){
        this.active();
    }

}
</script>
<style scoped>
.my-menu-bar—item{
    display: inline;
    font-size: 14px;
}

</style>


