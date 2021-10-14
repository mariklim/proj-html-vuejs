<template>
  <header>
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
    };
  },
  created() {
    this.newArrLinks.splice(this.newArrLinks.length - 1);
  },
};
</script>

<style lang="scss">
@import "../assets/style/common";
header {
  height: 4.375rem;
  top: 0;
  left: 0;
  width: 100%;
  background-color: transparent;
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-top: 1.25rem;
  padding: 1.875rem;

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
  .currentPage{
    border-bottom: 2px solid $main_color;
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