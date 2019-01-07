<template>
    <div class="column navarea">
        <div class="navbar">
            <div>
                <img src="http://placehold.it/200x70" alt="">
            </div>
            <div class="menu-btn">
                <a href="#" @click.prevent="isOpen = !isOpen">MENU</a>
            </div>
        </div>
        
        <div class=" nav" v-bind:class="{ open : isOpen }">
        <ul>
            <li><router-link to="/">Home</router-link></li>
            <li><router-link to="text-inputs">Text Inputs</router-link></li>
            <li><a href="#">Hyperlinks</a></li>
            <li><a href="#">Image Gallery</a></li>
            <li><a href="#">Buttons</a></li>
            <li><a href="#">Heading Text</a></li>
            <li><a href="#">Checkbox</a></li>
            <li><a href="#">Radio Button</a></li>
        </ul>
        </div>

    </div>

    


</template>
<script>
export default {
    data() {
        return {
            isOpen: true,
        }
    }  
}
</script>
<style lang="scss" >

    .navbar {
        background: red;
        display: grid;
        grid-template-columns: 3fr 1fr;
        padding: 1rem;
    }
    .navarea {
        background-color: black;
    }

.menu-btn {
    display: flex; justify-content: center; align-items: center;
}

@media (min-width: 801px) {

    .menu-btn {
        display: none;
    }

}


</style>
