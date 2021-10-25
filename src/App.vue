<template>
  <div id="app">
    <Header />
    <Hero />
    <main>
      <Products  />
      <Corporate />
      <Steps />
      <Contacts />
    </main>
    <Footer />
    <ScrollTopArrow></ScrollTopArrow>
   
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";

// Main
import Products from "./components/Main/Products.vue";
import Corporate from "./components/Main/Corporate.vue";
import Steps from "./components/Main/Steps.vue";
import Contacts from "./components/Main/Contacts.vue";
// Main

import Footer from "./components/Footer.vue";
import ScrollTopArrow from './ScrollTopArrow.vue';
export default {
  name: "App",
  components: {
    Header,
    Hero,

    // Main
    Products,
    Corporate,
    Steps,
    Contacts,
    // Main

    Footer,
    ScrollTopArrow,
  
  },
  data() {
    return {  
    };
  },
  
};
</script>
 

<style lang="scss">
@import "~@fortawesome/fontawesome-free/css/all.css";
@import "./assets/style/common";


</style>
