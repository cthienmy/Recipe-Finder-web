<script setup>

import itemFoodType from './components/itemFoodType.vue';
import GroupChoices from './components/GroupChoices.vue';
import pizzaImg from './assets/pizza.avif';
import riceImg from './assets/rice.jpeg';
import friedImg from './assets/fried.png';
import img1 from './assets/img1.jpeg';
import img2 from './assets/img2.jpeg';
import img3 from './assets/img3.jpeg';
import img4 from './assets/img4.jpeg';
import img5 from './assets/img5.jpeg';
import img6 from './assets/img6.jpeg';

</script>

<template>
  <div class="border-phone">
    <div class="header">
      <div class="title">
        <div class="title-text">Recipe Finder</div>
        <input class="input-recipe" />
      </div>
      <!--  -->
      <div class="group-food-type">

        <itemFoodType v-for="(itemFoodType, index) in groupFoodType" v-bind:itemFoodType="itemFoodType"
          v-bind:key="itemFoodType" />

      </div>
      <!--  -->
    </div>

    <div class="body">
      <!--  -->
      <div class="anh-bia">
        <img class="img-round" alt="anh bia" src="./assets/anhbia.jpg" width=100% height="150" />
      </div>
      <!--  -->
      <div class="suggestions">

        <GroupChoices v-for="(itemGroupChoices, index) in groupChoices" v-bind:itemGroupChoices="itemGroupChoices"
          v-bind:key="itemGroupChoices" />

      </div>
    </div>
    <!--  
  <main>
    <TheWelcome />
  </main>
  -->
  </div>
</template>



<script>
export default {
  name: "app",
  components: {
    itemFoodType,
  },
  data() {
    return {
      groupFoodType: [
        {
          imgItem: pizzaImg,
          imgTitle: "PIZAA"
        },
        {
          imgItem: riceImg,
          imgTitle: "RICE"
        },
        {
          imgItem: friedImg,
          imgTitle: "FRIED"
        }

      ],
      groupChoices: [
        {
          titleChoice: "Popular Choices",
          listItem: [
            {
              imgItemFood: img1,
              imgTitleFood: "Yam Fries"
            },
            {
              imgItemFood: img2,
              imgTitleFood: "Yam Fries"
            },
            // {
            //   imgItemFood: img3,
            //   imgTitleFood:"Yam Fries"
            // },
            // {
            //   imgItemFood: img4,
            //   imgTitleFood:"Yam Fries"
            // }
          ]
        },
        {
          titleChoice: "Best Desserts",
          listItem: [
            {
              imgItemFood: img1,
              imgTitleFood: "Yam Fries"
            },
            {
              imgItemFood: img2,
              imgTitleFood: "Yam Fries"
            },
            // {
            //   imgItemFood: img3,
            //   imgTitleFood:"Yam Fries"
            // },
            // {
            //   imgItemFood: img4,
            //   imgTitleFood:"Yam Fries"
            // }
          ]
        }
      ]
    }

  }
}
</script>

<style scoped>
/*  

header {
  line-height: 1.5;
}
  
.logo {
  display: block;
  margin: 0 auto 2rem;
}

@media (min-width: 1024px) {
  header {
    display: flex;
    place-items: center;
    padding-right: calc(var(--section-gap) / 2);
  }

  .logo {
    margin: 0 2rem 0 0;
  }

  header .wrapper {
    display: flex;
    place-items: flex-start;
    flex-wrap: wrap;
  }
  
}
*/
.border-phone {
  border: 5px solid black;
  border-radius: 35px;
  padding: 25px 10px;
  width: 360px;
  height: 740px;
}

.title {
  text-align: center;
}

.title-text {
  font-size: 35px;
  font-family: Georgia, 'Times New Roman', Times, serif;
  font-style: italic;
  font-weight: 700;
}

.input-recipe {
  width: 100%;
  padding: 8px;
  border-radius: 5px;

}

.group-food-type {
  display: flex;
  justify-content: space-between;
  width: 100%;
  margin: 10px 0;
}


.anh-bia {
  margin-top: 15px;
}

.img-round {
  border-radius: 10px;
  width: 100%;
}
</style>
