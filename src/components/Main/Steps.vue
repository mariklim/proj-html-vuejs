<template>
  <section>
    <section class="section_1">
      <div class="container_step">
        <div class="step_top">
          <div class="step_title">
            <h2>Tell us what you have in mind</h2>
          </div>
          <div class="number_step">01</div>
        </div>
        <div class="step_bottom">
          <div class="text">
            <h5>MANUAL INGREDIENTS SELECTION</h5>
            <p>
              Cras consequat lectus vestibulum tortor pulvinar, quis euismod
              nisl varius. Ut eu laoreet ex. Aliquam erat volutpat. Nullam quis
              sagittis nibh. Morbi consectetur ultricies ante ac congue. Donec
              lorem erat, finibus in velit placerat, rutrum augue.
            </p>
          </div>
        </div>
      </div>
    </section>
    <section class="section_2">
      <div class="container_step">
        <div class="box_left">
          <div class="step_top">
            <div class="step_title">
              <h2>We Start Baking</h2>
            </div>
            <div class="number_step">02</div>
          </div>
          <div class="step_bottom">
            <div class="text">
              <h5>SWEET & DELICIOUS</h5>
              <p>
                Cras consequat lectus vestibulum tortor pulvinar, quis euismod
                nisl varius. Ut eu laoreet ex. Aliquam erat volutpat. Nullam
                quis sagittis nibh. Morbi consectetur ultricies ante ac congue.
                Donec lorem erat, finibus in velit placerat, rutrum augue.
              </p>
            </div>
          </div>
        </div>
        <div class="box_right">
            <div class="text">
            <h5>DONT JUST TAKE OUR WORD FOR IT</h5>
            <h3>“Finally found an alternative to the mass produced products. Something that incorporates real organic ingredients, nutrient dense wellness while promoting sustainability and activity.”</h3>
            <h4>Rachel Cooper, Founder</h4>
            </div>
        </div>
      </div>
    </section>
     <section class="section_3">
      <div class="container_step">
        <div class="step_top">
          <div class="step_title">
            <h2>Delivered to your home</h2>
          </div>
          <div class="number_step">03</div>
        </div>
        <div class="step_bottom">
          <div class="text">
            <h5>BAKED TO ORDER & GIFT WRAPPED</h5>
            <p>
              Cras consequat lectus vestibulum tortor pulvinar, quis euismod
              nisl varius. Ut eu laoreet ex. Aliquam erat volutpat. Nullam quis
              sagittis nibh. Morbi consectetur ultricies ante ac congue. Donec
              lorem erat, finibus in velit placerat, rutrum augue.
            </p>
          </div>
        </div>
      </div>
    </section>
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
//STEP 1
.section_1 {
  @include container_80;
  @include section_header;
  @include margin_top_bottom_70px;
  height: 37.5rem;
  background-image: linear-gradient(
      170deg,
      rgba(35, 33, 37, 0.3) 0%,
      rgba(35, 33, 37, 0.8) 100%
    ),
    url("../../assets/image/bakery-process-1.jpg");
  background-size: cover;
  color: white;
}
//STEP 1

//STEP 2
.section_2 {
  @include container_80;
  @include section_header;
  @include margin_top_bottom_70px;
  height: 37.5rem;
  color: white;
  .container_step {
    width: 100%;
    display: flex;
    flex-direction: row;
  }
  .box_left {
       display: flex;
  flex-direction: column;
  justify-content: space-between;
    width: 50%;
    background-image: linear-gradient(
        170deg,
        rgba(35, 33, 37, 0.3) 0%,
        rgba(35, 33, 37, 0.8) 100%
      ),
      url("../../assets/image/bakery-process-2.jpg");
    background-size: cover;
    padding: 1.875rem;
    margin-right: 1.25rem;
    .step_bottom {
      display: flex;
      justify-content: start;
    }
  }
  .box_right {
      display: flex;
      justify-content: center;
      align-items: center;
    width: 50%;
    height: 100%;
    background-color: $main_color_light;
    padding: 3.125rem;
    color: $main_color;
    .text{
        width: 80%;
    }
  }
}
//STEP 2

.section_3 {
  @include container_80;
  @include section_header;
  @include margin_top_bottom_70px;
  height: 37.5rem;
  background-image: linear-gradient(
      170deg,
      rgba(35, 33, 37, 0.3) 0%,
      rgba(35, 33, 37, 0.8) 100%
    ),
    url("../../assets/image/bakery-process-3.jpg");
  background-size: cover;
  color: white;
}

//common  per STEP 1 ,2 e 3
.container_step {
  width: 80%;
  height: 100%;
  margin: auto;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  .step_top {
    display: flex;
    justify-content: space-between;
    align-items: center;
    padding: 1.25rem 0;
    .step_title {
      font-size: 20px;
    }
    .number_step {
      font-size: 3.75rem;
      font-weight: 200;
    }
  }
  .step_bottom {
    display: flex;
    justify-content: end;
    padding: 1.25rem 0;
    .text {
      width: 40%;
    }
  }
}
</style>