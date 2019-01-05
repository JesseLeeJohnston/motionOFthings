<template>



  <div class="grid">
<Nav></Nav>

    <nuxt/>
  </div>


</template>

<script>
import Nav from "~/components/Nav.vue";


export default {
  components: {
    Nav
  }
}

</script>


<style lang="sass">
  @import '../assets/sass/main.scss'
</style>

