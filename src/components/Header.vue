<template>
  <header>
    <div class="logo">
      <img src="../assets/image/avada-bakery-logo.png" alt="logo" />
    </div>
    <ul>
      <li>
        <Link v-for="(link, index) in links" :key="index" :link="link" />
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
      links: elm,
    };
  },
};
</script>

<style lang="scss">
@import "../assets/style/common";
header {
  height: 4.375rem;
  background-color: transparent;
  display: flex;
  justify-content: space-between;
  align-items: center;
  padding: 20px;


  ul{
     padding: 0 .625rem;
     li{
       a{
         padding: 0 1.25rem;
         font-size: .75rem;
         font-weight: 500;
       }
     }
      
    
  }

  .logo {
    width: 9.375rem;
    img {
      width: 100%;
    }
  }
}
</style>