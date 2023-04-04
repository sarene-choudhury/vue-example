<script>
import NavBar from './NavBar.vue'
import CartItem from './CartItem.vue'


export default {
    data() {
        return {
            hotdog: "default",
            itemCount: 0,
        }
    },
    components: {
        NavBar,
        CartItem,
    },
}



</script>
<template>
    <body>
        <CartItem
                image = '../assets/vintage.png' 
                productName = "Vintage Hot Dog"
                description = "A hotdog dressed up in vintage clothing"
                price = "2,000,000"

                @addItemToCart="$event => itemCount++"
        />
        <CartItem
                image = '../assets/patriotic.png' 
                productName = "Patriotic Hot Dog"
                description = "A hotdog patriotic enough for the fourth of july"
                price = "10,000,000"

                @addItemToCart-="$event => itemCount++"
        />
        <CartItem
                image = '../assets/beautiful.png' 
                productName = "Beautiful Hot Dog"
                description = "A hotdog all glammed up"
                price = "1,000,000"

                @addItemToCart="$event => itemCount++"
        />
        <CartItem
                image = '../assets/winner.png' 
                productName = "Winner Hot Dog"
                description = "A hotdog who has beaten Michael Phelps and is proud of it"
                price = "700,000,000"

                @addItemToCart="$event => itemCount++"
        />

    </body>
    The amount of hotdogs in your cart totals to {{ itemCount }}
    
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