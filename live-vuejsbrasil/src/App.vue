<template>
  <div>
    <h1 :style="{ color }">Hello {{ name }}</h1>
    <input type="text" v-model="name" />
    <button @click="handleClick">Alert!</button>
  </div>
</template>

<script>
export default {
  data() {
    return{
      name: 'Ihering',
      color: 'tomato'
    }
  },
  methods: {
    handleClick () {
      window.alert('clicado')
    }
  }
};
</script>
