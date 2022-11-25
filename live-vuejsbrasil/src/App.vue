<template>
  <!-- <div>
    <h1 :style="{ color }">Hello {{ name }}</h1>
    <input type="text" v-model="name" />
    <button @click="handleClick">Alert!</button>
  </div> -->

  <div>
    <h1>Minha lista</h1>
    <input type="text" v-model="currentFood" />
    <button @keyup.enter="addFood">Add</button>
    <ul>
      <li v-for="food in foods" :key="food">{{ food }}</li>
    </ul>
  </div>
</template>

<script>
export default {
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

    addFood() {
      this.foods.push(this.currentFood);
      this.currentFood = "";
    },
  },
};
</script>
