<template>

  <div class="grid">
    <div class="column nav" v-bind:class="{ open : isOpen }">
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
    <div class="column content">
      <div class="hero">
        <h1 class="">motionOFthings</h1>
        <p>I needed to practice css animations and I thought building out a repo with some sweet animations to different elements would be a good way to build my brains.</p>
        <a v-on:click='isOpen = !isOpen'>Menu</a>
      </div>
      
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

<style lang="scss" scoped>
  .nav {
    grid-area: nav;
    background-color: black;
    color: white;
    // height: 100vh;
    overflow: auto;
    ul {
      li {
        list-style: none;
        line-height: 3rem;
      }
    }
    a {
      color: white;
      text-decoration-line: overline;
    }
  }
  .content {
    grid-area: content;
  }

  .hero {
    display: flex;
    flex-direction: column;
    justify-content: center;
    height: 100vh;
    align-items: center;
    padding: 0 2rem;
    h1 {
      margin: 0;
    }
    p {
      margin: 0;
      max-width: 40rem;
    }
  }

  @media (max-width: 800px) { 
    .grid {
      display: grid;
      grid-template-columns: 1fr;
      grid-template-areas: 
        "nav"
        "content"
        ;
    }
    .nav {
      height: 0;
      transform: scaleY(0);
      transition: transform .3s .2s;
      &.open {
        height: auto;
        transform: scaleY(1);
        transition: transform .3s .2s;
      } 
    }
  }
  @media (min-width: 801px) { 
    .grid {
      display: grid;
      grid-template-columns: 1fr 3fr;
      grid-template-areas: 
        "nav content content content"
    }

  }

  // @media (min-width: 600px) { 

  // }


  // @media (min-width: 800px) { 

  // }


  // @media (min-width: 1200px) { 

  // }


  // @media (min-width: 1440px) { 

  // }




</style>


