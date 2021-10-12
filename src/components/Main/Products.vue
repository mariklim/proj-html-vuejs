<template>
  <section>
    <div class="container products">
      <div class="our_products">
        <div class="text">
          <h5 class="section_small_title">OUR PRODUCTS</h5>
          <h3 class="semibold_section_title">
            All our delectable pastries are backed fresh in our Kitchen very morning, and are made with all-natural, all organic ingredients.
          </h3>
        </div>
        <button class="btn_lilac">Explore our profucts</button>
      </div>
      <div class="prod_gallary">
          <ul>
              <li>
                  <a href="#">
                      
                      <img src="../../assets/image/choco-chip-cookies-400x510.jpg" alt="choco chip cookies">
                  </a>
                  <a href="#">
                      <img src="../../assets/image/strawberry-jam-cookies-400x510.jpg" alt="strawberry jam cookies">
                  </a>
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
        .our_products{
            width: 30%;
             & .text{
                 padding-right: 1.25rem;
             }
        
        }
        .prod_gallary{
            li{
                display: flex;
            }
            li a{
                margin: 0 .625rem;
                max-width: 25rem;
                img {
                    width: 100%;
                }
            }
        }
  }
}
</style>