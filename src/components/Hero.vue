<template>
  <section class="header-hero">
      <div class="container_80">
          Ciao
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
.header-hero {
  margin-top: -9.375rem;
  height: 56.25rem;
  background-image: url("../assets/image/hero-header-bakery.jpg");
  background-size: cover;
  background-repeat: no-repeat;
  background-position: center center;
  padding: 6.25rem 0;
}

.container_80{
    @include container_80;
    border: 1px solid white;
    margin-top: 200px;
}
</style>