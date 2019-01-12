<template>
    <div class="column navarea">
        <div class="navbar">
            <div style="display: flex; flex-direction: column;">
                <img class="logo" src="../assets/images/logo.svg" alt="">
            </div>
            <div class="menu-btn">
                <a href="#" @click.prevent="isOpen = !isOpen">MENU</a>
            </div>
        </div>
        
        <div class=" nav" v-bind:class="{ open : isOpen }">
        <ul>
            <li><router-link to="/">Home</router-link></li>
            <li><router-link to="text-inputs">Text Inputs</router-link></li>
            <li><router-link to="checkbox">Checkbox</router-link></li>
            <li><router-link to="buttons">Buttons</router-link></li>
            <li><router-link to="image-gallery">Image Gallery</router-link></li>
            <li><router-link to="typography">Typography</router-link></li>
            <li><router-link to="text-inputs">Text Inputs</router-link></li>
        </ul>
        </div>

    </div>

    


</template>
<script>
export default {
    data() {
        return {
            isOpen: false,
        }
    }  
}
</script>
<style lang="scss" >

    .navbar {
        background: #191a19;
        padding: 1rem;
        grid-area: navLogo;
        display: flex;
        justify-content: space-between;
    }
    .navarea {
        background-color: black;
        height: auto;
        overflow-y: auto;

    }

.logo {
    height: 1.5rem;
}

.menu-btn {
    display: flex; justify-content: center; align-items: center;
    a {
         color: #ffffff;
         text-decoration: none;
    }
}

@media (min-width: 801px) {

    .menu-btn {
        display: none;
    }
    .navarea {
        height: 100vh;
        width: 280px;
                position: fixed;
        top: 0px;
    }


}


</style>
