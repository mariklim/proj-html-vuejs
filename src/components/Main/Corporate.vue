<template>
  <section>
    <!--CORPORATE & WEDDINGS  -->
    <div v-scroll-reveal.reset="{ delay: 300}" class="corporate">
      <h5>CORPORATE & WEDDINGS</h5>
      <h3>Baking Special Moments</h3>
      <div class="corporate_cards">
        <div class="card corporate">
          <div class="card corporate active">
            <span>
              <h5>INTERNATIONAL BAKERY</h5>
              <h3>Corporate Events</h3>
              <button class="btn_lilac">Explore more</button>
            </span>
          </div>
        </div>
        <div v-scroll-reveal.reset="{ delay: 600}" class="card wedding">
          <div class="card wedding active">
            <span>
              <h5>PRIVATE DINING HALL</h5>
              <h3>Weddings & Parties</h3>
              <button class="btn_lilac">Explore more</button>
            </span>
          </div>
        </div>
      </div>
    </div>
    <!--/CORPORATE & WEDDINGS  -->

    <!-- SHOP gallery -->
    <div class="shop_gallery">
      <div v-scroll-reveal.reset="{ delay: 250}" class="text">
        <span>
          <h3>Find a freshly baked product perfect for you</h3>
          <p>
            Integer a nibh vitae ex porttitor rutrum et ut velit. Etiam ac felis
            at leo feugiat placerat. Sed ac nulla id orci tempor convallis sed.
          </p>
          <button class="btn_lilac">Shop all products</button>
        </span>
      </div>
      <div v-scroll-reveal.reset="{ delay: 300 }" class="prod_gallery">
        <Slider4 />
      </div>
    </div>

    <!-- /SHOP  gallery-->
  </section>
</template>

<script>
import Slider4 from "./Slider4.vue";
export default {
  name: "Corporate",
  components:{
 Slider4 
  }
}
</script>

<style lang="scss">
@import "../../assets/style/common";
@import "../../assets/style/variables";
@import "../../assets/style/Gallery";

.corporate {
  @include section_header;
  @include container_80;
  //   @include margin_top_bottom_70px;
  text-align: center;
  .corporate_cards {
    @include margin_top_bottom_70px;
    display: flex;
    justify-content: space-between;
    .card {
      width: 37.5rem;
      height: 40.625rem;
      background-color: coral;
      &.corporate {
        background-image: url("../../assets/image/corporate-bg.jpg");
        background-size: cover;

        //card al hover
        &.active {
          background-image: url("../../assets/image/corporate-hover-bg.jpg");
        }
      }
      &.wedding {
        background-image: url("../../assets/image/wedding-bg.jpg");
        background-size: cover;

        //card al hover
        &.active {
          background-image: url("../../assets/image/wedding-hover-bg.jpg");
        }
      }
      .active {
        display: flex;
        justify-content: center;
        align-items: center;
        color: white;
        text-align: center;
        opacity: 0;
        transition: opacity 1s;
      }
    }

    //Hover
    .card.corporate:hover .card.corporate.active {
      opacity: 1;
    }
    .card.wedding:hover .card.wedding.active {
      opacity: 1;
    }
  }
}
//SHOP
.shop_gallery {
  @include section_header;
  @include container_80;
  display: flex;
  .text {
    display: flex;
    justify-content: center;
    align-items: center;
    width: 25%;
    text-align: center;
  
    h3 {
      padding: 0;
    }
    p {
      padding-top: 0.625rem;
      padding-bottom: 0.625rem;
      font-size: 0.75rem;
      line-height: 1.25rem;
    }
    span{
      margin-right: 3.75rem;
    }
  }
}
</style>