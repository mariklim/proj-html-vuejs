<template>
  <section>
    <div class="products">
      <div class="our_products">
        <div class="text">
          <h5>OUR PRODUCTS</h5>
          <h3>
            All our delectable pastries are backed fresh in our Kitchen very
            morning, and are made with all-natural, all organic ingredients.
          </h3>
        </div>
        <button class="btn_lilac">Explore our products</button>
      </div>
      <div class="prod_gallery">
             <Slider />
      </div>
      <!-- <div class="prod_gallery">
        <ul>
          <li v-for="image in newArrImg" :key="image.id">
            <div class="cardImg">
              <div class="img">
                <img :src="image.src" :alt="image.name" />
                <div class="img_cover">
                  <div class="description">
                    <h4>{{ image.name }}</h4>
                    <p>{{ image.type }}</p>
                    <h4 class="price">{{ image.price }}</h4>
                  </div>
                </div>
              </div>
            </div>
          </li>
        </ul>
      </div> -->
    </div>
  </section>
</template>

<script>
import Slider from "./Slider.vue";
export default {
  name: "Products",
  components:{
    Slider
  },
  props: {
    imagesArr: Array,
  },
  data() {
    return{
      newArrImg:this.imagesArr,
    }
  },

  //per stampare solo 2 foto da arr
  created() {
    this.newArrImg.splice(this.newArrImg.length - 2, 3);
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