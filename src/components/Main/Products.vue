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
        <ul>
          <li>
            <div class="cardImg">
              <div class="img">
                <img
                  src="../../assets/image/choco-chip-cookies-500x638.jpg"
                  alt="choco chip cookies"
                />
                <div class="img_cover">
                  <div class="description">
                    <h4>Choco chip cookies</h4>
                    <p>Coocies, Pastries</p>
                    <h4 class="price">$18.00 – $32.00</h4>
                  </div>
                </div>
              </div>
            </div>
          </li>
          <li>
            <div class="cardImg">
              <div class="img">
                <img
                  src="../../assets/image/strawberry-jam-cookies-500x638.jpg"
                  alt="strawberry jam cookies"
                />
                <div class="img_cover">
                  <div class="description">
                    <h4>Strawberry jam cookies</h4>
                    <p>Coocies, Pastries</p>
                    <h4 class="price">$18.00 – $32.00</h4>
                  </div>
                </div>
              </div>
            </div>
          </li>
        </ul>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Products",
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
    width: 30%;
    & .text {
      padding-right: 1.25rem;
    }
  }
}
</style>