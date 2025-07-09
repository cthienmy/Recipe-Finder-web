<template>
    <div class="popular-choices">
          <div>{{itemGroupChoices.titleChoice}}</div>
          <!-- llist-popula -->
        <div class="list-popular">
          <!-- item-food -->
          <ItemFood v-for="(itemFood, index) in itemGroupChoices.listItem" v-bind:itemFood="itemFood"/>
        </div>
    </div>
</template>
<script>
import ItemFood from './groupChoice/ItemFood.vue';

export default{
    name:"GroupChoices",
    props:{
      itemGroupChoices: Object,
    },
    components:{
      ItemFood,
    }
}
</script>
<style>
.list-popular{
  display: flex;
}
</style>