<template>
    <h1 :style="{ textDecoration: decoration }">Hello {{ name }}</h1>
    <input type="text" v-model="name">
    <br/>

    <a href="link">Google</a>
</template>

<script>
export default {
data: () => ({
    name: 'Ihering',
    link: 'https://google.com',
    decoration: 'underline'
})
}
</script>
