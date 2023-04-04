<script>
import beautiful from '../assets/beautiful.png' 
import vintage from '../assets/vintage.png' 
import winner from '../assets/winner.png' 
import patriotic from '../assets/patriotic.png' 

export default{
    props: [
        "image",
        "productName",
        "description",
        "price",
    ],
    methods: {
        addItemToCart(productName) {this.$emit('addItemToCart', productName)}
    }, 
}

</script>
<template>
    <div class="item">
        <img :src="image" alt="hotdog">
        <h2>productName: {{ productName }}</h2>
        <h2>description: {{ description }}</h2>
        <h2>price: {{ price }}</h2>
        <button @click="addItemToCart(productName)">Add Item to Cart</button>
    </div>
</template>


<style scoped>
img {
    display: block;
    margin-left: auto;
    margin-right: auto;
}

.links {
    display: flex;
    justify-content: space-evenly;
}
</style>