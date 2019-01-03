<template>

  <div class="grid">
    <div class="column">
      <img src="http://placehold.it/300x80" alt="">
      <ul>
        <li><a href="#">Home</a></li>
        <li><a href="#">Text Inputs</a></li>
        <li><a href="#">Hyperlinks</a></li>
        <li><a href="#">Image Gallery</a></li>
        <li><a href="#">Buttons</a></li>
        <li><a href="#">Heading Text</a></li>
        <li><a href="#">Checkbox</a></li>
        <li><a href="#">Radio Button</a></li>
      </ul>
    </div>
    <div class="column">The is main page content area</div>
  </div>

</template>

<script>

export default {

}
</script>

<style lang="scss" scoped>

  .grid {
    display: grid;
        grid-template-columns: 1fr 3fr;

  }
  .column {
  }

</style>


