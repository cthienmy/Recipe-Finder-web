<template>
 
    
    <div class="item-food">
      <img class="img-item-food" v-bind:src="itemFood.imgItemFood" width="120" height="100"/>
      <div>{{itemFood.imgTitleFood}}</div>
    </div>
    

 
</template>


<script>


export default {
  name: "ItemFood",
    props: {
     itemFood: Object,
  }
}
</script>
<style>
.item-food{
  margin-right: 10px;
}
.img-item-food{
  
}
</style>