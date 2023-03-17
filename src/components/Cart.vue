<script>
import NavBar from './NavBar.vue'


export default {
    components: {
        NavBar,
    }
}

</script>
<template>
    <body>
        <NavBar></NavBar>
        <img :src="src" alt="hotdog">
        <div class="links">
        </div>

    </body>
</template>