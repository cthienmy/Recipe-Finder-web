

<template>
<!-- 
  <div class="greetings">
    <h1 class="green">{{ msg }}</h1>
    <h3>
      You’ve successfully created a project with
      <a href="https://vite.dev/" target="_blank" rel="noopener">Vite</a> +
      <a href="https://vuejs.org/" target="_blank" rel="noopener">Vue 3</a>.
    </h3>
  </div>
   -->
   <div class="item-food-type">
          <img class="img-round" v-bind:src="itemFoodType.imgItem" width="90" height="60" />
          <a class="link-foods" href="#"><div class="link-food-type">{{ itemFoodType.imgTitle}}</div></a>
   </div>
</template>
<script>
import GroupChoices from './GroupChoices.vue';

   export default {
    name: "itemFoodType",
    props:{
      itemFoodType: Object,
      groupChoices: Object,
    }
   }
</script>

<style scoped>
.item-food-type {
  width: 100px;
  
}

.link-food-type {
  text-align: center;
}
.link-foods{
  
}
.img-round {
  border-radius: 10px;
  width: 100%;
}
/*  
h1 {
  font-weight: 500;
  font-size: 2.6rem;
  position: relative;
  top: -10px;
}

h3 {
  font-size: 1.2rem;
}

.greetings h1,
.greetings h3 {
  text-align: center;
}

@media (min-width: 1024px) {
  .greetings h1,
  .greetings h3 {
    text-align: left;
  }
}
*/
</style>
