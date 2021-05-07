<template>
  <div class="tab-bar-item" @click="itemClick">
<!--    所有的item都展示同一个图片和文字-->
    <div v-if="!isActive"> <slot name="item-icon"></slot></div>
    <div v-else><slot name="item-icon-active"></slot></div>
<!--    <div :class="{active:isActive}"><slot name="item-text"></slot></div>-->
    <div :style="activeStyle"><slot name="item-text"></slot></div>

  </div>
</template>

<script>
    export default {
        name: "TabBarItem",
        props:{
          path:String,
          activeColor:{
            type:String,
            default:"red"
          }
        },
        data(){
          return {
            // isActive: true
          }
        },
        computed:{
          isActive(){
            //  /home->item1(/home)=true
            //  /home->item1(/category)=false
            //  /home->item1(/cart)=false
            //  /home->item1(/profile)=false
            // 找到的话值就 不是-1 返回值就是true
            return this.$route.path.indexOf(this.path)!=-1
          },
          activeStyle(){
            return this.isActive ?{color:this.activeColor}:{}
          }
        },
        methods:{
          itemClick(){
            // console.log('itmclick');
            //进行跳转的功能
            // this.$router.push()
          this.$router.replace(this.path)
          }
        }
    }
</script>

<style scoped>
  .tab-bar-item{
    flex: 1;
    text-align: center;
    height: 49px;
    font-size: 14px;
    /*line-height: 49px;*/
  }
  .tab-bar-item img{
    /*display: none;*/
    width: 24px;
    height: 24px;
    margin-top: 3px;
    /*去除图片和文件之间的像素*/
    vertical-align: middle;
    margin-bottom: 2px;
    /*overflow: hidden;*/
  }


</style>
