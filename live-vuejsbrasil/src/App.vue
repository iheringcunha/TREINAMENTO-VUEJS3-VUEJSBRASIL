<template>
  <!-- <div>
    <h1 :style="{ color }">Hello {{ name }}</h1>
    <input type="text" v-model="name" />
    <button @click="handleClick">Alert!</button>
  </div> -->

  <div>
    <h1>Minha lista</h1>
    <input @keyup.enter="addFood" type="text" v-model="currentFood" />
    <button @click="addFood">Add</button>
    <!-- <food-list @my-event="handleClick" :foods="foods"/> -->
    <food-list @stop="handleStop" :foods="foods"/>
  </div>
</template>

<script>
import FoodList from './components/FoodList.vue'
export default {
  components : {
    FoodList
  },

  data() {
    return {
      // name: 'Ihering',
      // color: 'tomato'

      foods: ["maçã", "pêra"],
      currentFood: "",
    };
  },
  methods: {
    // handleClick () {
    //   window.alert('clicado')
    // }

    handleStop (payload) {
      console.log('payload =>', payload)
      window.alert(payload) 
    },

    addFood() {
      this.foods.push(this.currentFood);
      this.currentFood = "";
    },
  },
};
</script>
