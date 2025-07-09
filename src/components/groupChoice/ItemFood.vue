<template>
 
    
    <div class="item-food">
      <img v-bind:src="itemFood.imgItemFood"/>
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
  width: 120px;
}
</style>