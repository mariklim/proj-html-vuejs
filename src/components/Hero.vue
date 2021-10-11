<template>
  <section class="header-hero">
    <div class="container_80">
      <div class="text">
        <h5>FRESH & TASTY BAKERY EVERY DAY</h5>
        <h2>The Perfect Fresh Bread</h2>
        <p>
          Cras consequat lectus vestibulum tortor pulvinar, quis euismod nisl
          varius. Aliquam erat volutpat. Nullam quis sagittis nibh ac nulla id
          orci tempor.
        </p>
      </div>
      <button class="btn_white">Explore our profucts</button>
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
.header-hero {
  margin-top: -9.375rem;
  height: 56.25rem;
  background-image: url("../assets/image/hero-header-bakery.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  padding: 6.25rem 0;
}

.container_80 {
  @include container_80;
  margin-top: 200px;
  .text {
    width: 40%;
    h2 {
      padding-top: .9375rem;
      font-family: "Lora", serif;
      font-size: 1.875rem;
    }
    h5 {
      font-weight: 400;
      font-size: 0.625rem;
    }
    p {
      font-size: 0.8125rem;
      line-height: 1.25rem;
      padding: 1.5625rem 0;
    }
  }
}
</style>