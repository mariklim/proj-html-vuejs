<template>
  <div id="app">
    <Header/>
    <Hero />
    <main>
      
      <Products :imagesArr="imagesArr" />
      <Corporate />
      <Steps />
      <Contacts />
      
     
    </main>
    <Footer />
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
  data(){
    return{
      imagesArr:[
    {   
        name: "Choco Chip Cookies",
        src: require("./assets/image/choco-chip-cookies-400x510.jpg"),
        price:"$18.00 – $32.00",
        type:"Coocies, Pastries"
    },
    {   
        name: "Strawberry Jam Cookies",
        src: require("./assets/image/strawberry-jam-cookies-400x510.jpg"),
        price:"$18.00 – $32.00",
        type:"Coocies, Pastries"
    },
    {   
        name: "Strawberry Donut",
        src: require("./assets/image/strawberry-donut-400x510.jpg"),
        price:"$18.00 – $32.00",
        type:"Coocies, Pastries"
    },
    {   
        name: "Perfect Macarons",
        src: require("./assets/image/perfect-macarons-400x510.jpg"),
        price:"$18.00 – $32.00",
        type:"Coocies, Pastries"
    }
]
    }
  }
};
</script>,
 

<style lang="scss">
@import "~@fortawesome/fontawesome-free/css/all.css";
@import "./assets/style/common";
</style>
