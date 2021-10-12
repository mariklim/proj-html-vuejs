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
        <button class="btn_lilac">Explore our profucts</button>
      </div>
      <div class="prod_gallery">
        <ul>
          <li>
            <button class="btn_prev_next btn_prev">
              <i class="fas fa-chevron-left"></i>
            </button>
            <a class="margin_left_10" href="#">
              <img
                src="../../assets/image/choco-chip-cookies-400x510.jpg"
                alt="choco chip cookies"
              />
            </a>
            <a href="#">
              <img
                src="../../assets/image/strawberry-jam-cookies-400x510.jpg"
                alt="strawberry jam cookies"
              />
            </a>
            <button class="btn_prev_next btn_next">
              <i class="fas fa-chevron-right"></i>
            </button>
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
.products {
  @include container_80;
  @include section_header;
  @include margin_top_bottom_70px;
  display: flex;
  justify-content: space-between;
  // margin-top: 4.375rem;
  // margin-bottom: 4.375rem;
  .our_products {
    width: 30%;
    & .text {
      padding-right: 1.25rem;
    }
  }
  .prod_gallery {
    li {
      display: flex;
      align-items: center;
      position: relative;
    }
    li a {
      max-width: 25rem;
      img {
        width: 100%;
      }
    }
    button.btn_next {
      position: absolute;
      left: calc(100% - 1.875rem);
    }
    button.btn_prev {
      position: absolute;
      right: calc(100% - 1.875rem);
    }
  }
  //margin destro per spaziare immagini per first child per tag a
  .margin_left_10 {
    margin-right: 0.625rem;
  }
}
</style>