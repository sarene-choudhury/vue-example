<script>
import NavBar from './NavBar.vue'
import CartItem from '.CartItem.vue'


export default {
    components: {
        NavBar,
        CartItem,
    },
    data() {
        return {
            hotdog: "default",
            itemCount: 0,
        }
    }
}



</script>
<template>
    <body>
        <NavBar></NavBar>
        <img :src="src" alt="hotdog">
        <div class="links">
        </div>

        <CartItem>
                image = '../assets/vintage.png' 
                productName = "Vintage Hot Dog"
                description = "A hotdog dressed up in vintage clothing"
                price = "2,000,000"

                @add-to-cart="$event => itemCount++"
        </CartItem>
        <CartItem>
                image = '../assets/patriotic.png' 
                productName = "Patriotic Hot Dog"
                description = "A hotdog patriotic enough for the fourth of july"
                price = "10,000,000"

                @add-to-cart="$event => itemCount++"
        </CartItem>
        <CartItem>
                image = '../assets/beautiful.png' 
                productName = "Beautiful Hot Dog"
                description = "A hotdog all glammed up"
                price = "1,000,000"

                @add-to-cart="$event => itemCount++"
        </CartItem>
        <CartItem>
                image = '../assets/winner.png' 
                productName = "Winner Hot Dog"
                description = "A hotdog who has beaten Michael Phelps and is proud of it"
                price = "700,000,000"

                @add-to-cart="$event => itemCount++"
        </CartItem>

    </body>
    The amount of hotdogs in your cart totals to {{ itemCount }}
    
</template>