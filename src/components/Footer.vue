<template>
  <section class="footer-hero">
    <div class="container hero">
      <div class="text">
        <h5>TRY OUR SEASONAL PRODUCTS</h5>
        <h3>Order for pick-up or delivery to your home</h3>
      </div>
      <button class="btn_white">Shop Now</button>
    </div>
  </section>
</template>

<script>
export default {
  name: "Hero",
};
</script>

<style lang="scss">
@import "../assets/style/variables.scss";
@import "../assets/style/common.scss";

.footer-hero {
  @include margin_top_bottom_70px;
  @include section_header;
  background-image: url("../assets/image/call-to-action-bg.jpg");
  background-size: cover;
  padding: 5rem 0;
  color: white; 
  .container {
    &.hero {
      padding-left: 5rem;
      background-color: transparent;
      @include container_80;
      .text {
        width: 60%;
        h2 {
          font-family: "Lora", serif;
          font-size: 3.125rem;
        }
      }
    }
  }
}
</style>