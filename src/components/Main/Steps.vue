<template>
  <section>
      <div class="container_step">
          <div class="step_top">
              <div class="step_title">
                  <h2>Tell us what you have in mind</h2>

              </div>
              <div class="number_step">
                  01

              </div>
          </div>
          <div class="step_bottom"></div>
      </div>
  </section>
</template>

<script>
export default {
  name: "Steps",
  components: {},
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common";
@import "../../assets/style/variables";
section {
  @include container_80;
  @include section_header;
  @include margin_top_bottom_70px;
  height: 37.5rem;
  background-image: linear-gradient(
170deg, rgba(35, 33, 37, 0.3) 0%, rgba(35, 33, 37, 0.8) 100%),url("../../assets/image/bakery-process-1.jpg");
  background-size: cover;
   color: white;
}
.container_step{
    width: 80%;
    margin: auto;
    .step_top{
        display: flex;
        justify-content: space-between;
        align-items: center;
        padding: 1.25rem 0;
            .step_title{
                font-size: 20px;
            }
            .number_step{
                font-size: 3.75rem;
                font-weight: 200;
            }

    }
}
</style>