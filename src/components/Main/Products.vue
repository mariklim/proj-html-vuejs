<template>
  <section>
    <div class="container products">
      <div class="our_products">
        <div class="text">
          <h5 class="section_small_title">OUR PRODUCTS</h5>
          <h3 class="semibold_section_title">
            All our delectable pastries are backed fresh in our Kitchen very
            morning, and are made with all-natural, all organic ingredients.
          </h3>
        </div>
        <button class="btn_lilac">Explore our profucts</button>
      </div>
      <div class="prod_gallary">
        <ul>
          <li>
              <button class="btn_prev_next btn_prev"><i class="fas fa-chevron-left"></i></button>
            <a href="#">
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
             <button class="btn_prev_next btn_next"><i class="fas fa-chevron-right"></i></button>
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
.container {
  &.products {
    @include container_80;
    display: flex;
    margin-top: 3.125rem;
    margin-bottom: 3.125rem;
    .our_products {
      width: 30%;
      & .text {
        padding-right: 1.25rem;
      }
    }
    .prod_gallary {
      li {
        display: flex;
        align-items: center;
      }
      li a {
        max-width: 25rem;
        img {
          width: 100%;
        }
      }
      button.btn_next{
          position: relative;
          right:1.875rem;
      }
      button.btn_prev{
          position: relative;
          left:1.875rem;
      }
    }
  }
}
</style>