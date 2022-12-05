<template>
  <div>
    <h1 :style="{ textDecoration: decoration }">Hello {{ name }}</h1>
    <input type="text" v-model="name">
    <br/>

    <a :href="link">Google</a>
  </div>
</template>

<script>
export default {
data: () => ({
    name: 'Fulano',
    decoration: 'underline',
    link: 'http://google.com'
})
}
</script>

<style>

</style>