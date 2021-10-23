<template>
  <header :class="{change_color: scrollPosition > 50}">
    <div class="logo">
      <img src="../assets/image/avada-bakery-logo.png" alt="logo" />
    </div>
    <ul>
      <li>
        <Link v-for="(link, index) in newArrLinks" :key="index" :link="link" />
        <a href="#"><i class="fas fa-shopping-cart"></i></a>
      </li>
    </ul>
  </header>
</template>

<script>
import elm from "./Date/links.json";
import Link from "./Date/Link.vue";

export default {
  name: "Header",
  components: {
    Link,
  },
  data() {
    return {
      newArrLinks: elm,
      scrollPosition: null,
    };
  },
  methods: {
    updateScroll() {
       this.scrollPosition = window.scrollY
    }
},
mounted() {
    window.addEventListener('scroll', this.updateScroll);
}
};
</script>

<style lang="scss">
@import "../assets/style/common";
header {
  height: 4.375rem;
  top: 0;
  left: 0;
  width: 100%;
  background-color: rgba(255, 255, 255, 0) ;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 1.875rem;
  overflow: hidden;
  position: fixed;
  top: 0;
  z-index: 10;
   &.change_color {
       background-color:rgb(255, 255, 255)
   }


  ul {
    padding: 0 0.625rem;
    li {
      a {
        margin: 0 1.25rem;
        font-size: 0.75rem;
        font-weight: 500;
        text-transform: uppercase;
        display: inline-block;
        padding-bottom: 0.625rem;
        border-bottom: 2px solid transparent;
        transition: border-bottom 0.3s;
      }
    }
  }
 
  a:hover {
    border-bottom: 2px solid $main_color;
  }

  .logo {
    width: 9.375rem;
    img {
      width: 100%;
    }
  }
}
</style>