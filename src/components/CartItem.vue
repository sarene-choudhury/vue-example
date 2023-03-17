<script>
import NavBar from './NavBar.vue'


export default{
    props: [
        "image",
        "productName",
        "description",
        "price",
    ],
    methods: {
        addItemToCart(productName) 
        {this.$emit('addItemToCart', productName)}
    },
}

</script>
<template>
    <body>
        <NavBar></NavBar>
        <img :src="src" alt="hotdog">
        <div class="links">
        </div>
    </body>
    <div class="item">
        <h1>image: {{ image }}</h1>
        <h2>productName: {{ productName }}</h2>
        <h3>description: {{ description }}</h3>
        <h4>price: {{ price }}</h4>
        <button @click="addItemToCart(productName)"></button>
    </div>
</template>