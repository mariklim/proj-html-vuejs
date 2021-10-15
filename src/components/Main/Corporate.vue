<template>
  <section>
    <!--CORPORATE & WEDDINGS  -->
    <div class="corporate">
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
        <div class="card wedding">
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
      <div class="text">
        <span>
          <h3>Find a freshly baked product perfect for you</h3>
          <p>
            Integer a nibh vitae ex porttitor rutrum et ut velit. Etiam ac felis
            at leo feugiat placerat. Sed ac nulla id orci tempor convallis sed.
          </p>
          <button class="btn_lilac">Shop all products</button>
        </span>
      </div>
      <div class="prod_gallery">
        <ul>
          <li>
            <div class="cardImg">
              <div class="img">
                <img
                  src="../../assets/image/choco-chip-cookies-400x510.jpg"
                  alt="choco chip cookies"
                />
                <div class="img_cover">
                  <div class="description">
                    <h4>SELECT OPTIONS /</h4>
                    <h5>QUICK VIEW</h5>
                  </div>
                </div>
              </div>
              <div class="description">
                <h4>Choco chip cookies</h4>
                <h5>$18.00 – $32.00</h5>
              </div>
            </div>
          </li>
          <li>
            <div class="cardImg">
              <div class="img">
                <img
                  src="../../assets/image/strawberry-jam-cookies-400x510.jpg"
                  alt="strawberry jam cookies"
                />
                <div class="img_cover">
                  <div class="description">
                    <h4>SELECT OPTIONS /</h4>
                    <h5>QUICK VIEW</h5>
                  </div>
                </div>
              </div>
              <div class="description">
                <h4>Strawberry Jam Cookies</h4>
                <h5>$18.00 – $32.00</h5>
              </div>
            </div>
          </li>
          <li>
            <div class="cardImg">
              <div class="img">
                <img
                  src="../../assets/image/strawberry-donut-400x510.jpg"
                  alt="Strawberry Donut"
                />
                <div class="img_cover">
                  <div class="description">
                    <h4>SELECT OPTIONS /</h4>
                    <h5>QUICK VIEW</h5>
                  </div>
                </div>
              </div>
              <div class="description">
                <h4>Strawberry Donut</h4>
                <h5>$18.00 – $32.00</h5>
              </div>
            </div>
          </li>
           <li>
            <div class="cardImg">
              <div class="img">
                <img
                  src="../../assets/image/perfect-macarons-400x510.jpg"
                  alt="Perfect Macarons"
                />
                <div class="img_cover">
                  <div class="description">
                    <h4>SELECT OPTIONS /</h4>
                    <h5>QUICK VIEW</h5>
                  </div>
                </div>
              </div>
              <div class="description">
                <h4>Perfect Macarons</h4>
                <h5>$18.00 – $32.00</h5>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>

    <!-- /SHOP  gallery-->
  </section>
</template>

<script>
export default {
  name: "Corporate",
  
};
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
    margin-right: 1.25rem;
    h3 {
      padding: 0;
    }
    p {
      padding-top: 0.625rem;
      padding-bottom: 0.625rem;
      font-size: 0.75rem;
      line-height: 1.25rem;
    }
  }

}
</style>