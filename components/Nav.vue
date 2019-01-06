<template>
    <div class="column nav" v-bind:class="{ open : isOpen }">
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

</style>
