<template>
  <div id="app">
    <Header />
    <Hero />
    <main>
      Main
      <Products />
      <Corporate />
      <Steps />
      <Contacts />
      Fine Main
     
    </main>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Hero from "./components/Hero.vue";

// Main
import Products from "./components/Products.vue";
import Corporate from "./components/Corporate.vue";
import Steps from "./components/Steps.vue";
import Contacts from "./components/Contacts.vue";
// Main

import Footer from "./components/Footer.vue";

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

    Footer
  },
};
</script>,
 

<style lang="scss">
</style>
