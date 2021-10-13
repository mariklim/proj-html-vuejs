<template>
  <section>
    <div class="text">
      <h5>LOCATIONS</h5>
      <h3>Visit our Bakeries</h3>
    </div>
    <div class="container_contacts">
      <div class="contact">
        <div class="contact_img">
          <img src="../../assets/image/new-york-bk-600x397.jpg" alt="bakery" />
        </div>
        <div class="adress NY">
          <h3>New York</h3>
          <div class="adress_data">
            <div class="phon_number">
              <h5>CALL US</h5>
              <p>1.800.458.556</p>
            </div>
            <div class="hours_open">
              <h5>OPEN ALL WEEK</h5>
              <p>9:00 AM – 6:00 PM</p>
            </div>
            <button class="btn_white">View Map</button>
          </div>
        </div>
      </div>
      <div class="contact">
        <div class="contact_img">
          <img src="../../assets/image/london-bk-600x397.jpg" alt="bakery" />
        </div>
        <div class="adress LONDON">
          <h3>london</h3>
          <div class="adress_data">
             <div class="phon_number">
              <h5>CALL US</h5>
              <p>1.800.458.556</p>
            </div>
            <div class="hours_open">
              <h5>OPEN ALL WEEK</h5>
              <p>9:00 AM – 6:00 PM</p>
            </div>
            <button class="btn_white">View Map</button>
          </div>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: "Contacts",
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common";
@import "../../assets/style/variables";
section {
  @include margin_top_bottom_70px;
  @include container_80;
  @include section_header;
  .text {
    text-align: center;
  }
  .container_contacts {
    display: flex;
    .adress {
      text-align: center;
      &.NY {
        background-color: $sky;
      }
      &.LONDON {
        background-color: $light_pink;
      }
      .adress_data {
    
        display: flex;
        justify-content: space-around;
        align-items: center;
        padding-bottom: 1.875rem;

         p{
           padding: .1875rem 0
         }
      }
    }
  }
}
</style>