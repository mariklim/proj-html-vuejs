<template>
  <section >
    <div class="products">
      <div class="our_products">
        <div  v-scroll-reveal.reset="{ delay: 100}" class="text">
          <h5>OUR PRODUCTS</h5>
          <h3>
            All our delectable pastries are backed fresh in our Kitchen very
            morning, and are made with all-natural, all organic ingredients.
          </h3>
        </div>
        <button class="btn_lilac">Explore our products</button>
      </div>
      <div v-scroll-reveal.reset="{ delay: 150}" class="prod_gallery">
             <Slider2 />
      </div>
    </div>
  </section>
</template>

<script>
import Slider2 from "./Slider2.vue";
export default {
  name: "Products",
  components:{
    Slider2,
  },

  
};
</script>

<style lang="scss">
@import "../../assets/style/common";
@import "../../assets/style/variables";
@import "../../assets/style/Gallery";
.products {
  @include container_80;
  @include section_header;
  @include margin_top_bottom_70px;
  display: flex;
  justify-content: space-between;
  .our_products {
    width:calc(30% - 3.125rem);
    padding-right: 3.125rem;
    // & .text {
    //   padding-right: 1.25rem;
    // }
  }
}
</style>