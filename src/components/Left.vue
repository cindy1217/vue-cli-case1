<template>
  <div>
    <div class="title">热门推荐</div>
    <ul class="menu">
      <li @click="menu1">猫猫</li>
      <li @click="menu2">狗狗</li>
      <li @click="menu3">花花</li>
      <li @click="menu4">兔兔</li>
      <li @click="menu5">树木</li>
      <li @click="menu6">建筑</li>
      <li @click="menu7">水果</li>
    </ul>
    <!-- <Msg></Msg> -->
  </div>
</template>
<style type="text/css">
  .title{
    width: 100px;
    color: red;
    line-height: 34px;
  }
  .menu li{
       list-style: none;
       height: 50px;
       line-height: 50px;
       margin-bottom: 2px;
       background-color: #fff;
       cursor: pointer;
  }
  .menu li:hover{
     color: red;
  }
</style>
<script type="text/javascript">
import Msg from "./msg.js";
export default {
    methods:{
      menu1:function(){
        Msg.$emit("val","1")
      },
      menu2:function(){
        Msg.$emit("val","2")
      },
      menu3:function(){
        Msg.$emit("val","3")
      },
      menu4:function(){
        Msg.$emit("val","4")
      },
      menu5:function(){
        Msg.$emit("val","5")
      },
       menu6:function(){
        Msg.$emit("val","6")
      },
       menu7:function(){
        Msg.$emit("val","7")
      }
    },
  // components:{
  //   Msg
  // }
}
</script>