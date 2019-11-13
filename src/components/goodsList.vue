<template>
  <div name="show">
    <ul class="goodList">
      <li v-for="good in list">
        <img v-bind:src="good.img">
        <p>{{good.goodName}}</p>
      </li>
    </ul>
  </div>
</template>
<style>
 .goodList li{
   width: 200px;
   height: 200px;
   list-style: none;
   float: left;
   font-size: 12px;
   color: red;
   margin-bottom: 30px;
 }
 .goodList img{
   width: 180px;
   height: 180px;
 }
</style>
<script>
export default {
  name:"show",
  data(){
    var obj = this;
    var url = "";
    if(obj.goodId==1){
      url="json/cat.json";
    }else if(obj.goodId==2){
      url="json/dog.json";
    }else if(obj.goodId==3){
      url="json/flower.json"
    }else if(obj.goodId==4){
      url="json/rabbit.json"
    }else if(obj.goodId==5){
      url="json/tree.json"
    }else if(obj.goodId==6){
      url="json/build.json"
    }else if(obj.goodId==7){
      url="json/fruits.json"
    }else{
      url="json/fruits.json"
    }
    this.$http.get(url).then(function(res){
      obj.list=res.data;
    })
    return{
      list:[]
    }
  },
  props:{
    goodId:Number
  },
  watch:{
    goodId(){
      var obj = this;
      var url ="";
      if(obj.goodId==1){
        url="json/cat.json"
      }else if(obj.goodId==2){
        url="json/dog.json"
      }else if(obj.goodId==3){
        url="json/flower.json"
      }else if(obj.goodId==4){
        url="json/rabbit.json"
      }else if(obj.goodId==5){
        url="json/tree.json"
      }else if(obj.goodId==6){
        url="json/build.json"
      }else if(obj.goodId==7){
        url="json/fruits.json"
      }else{
        url="json/fruits.json"
      }
      this.$http.get(url).then(function(res){
        obj.list=res.data;
      })
      return{
        list:[]
      }
    }
  }
}
</script>