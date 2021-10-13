<template>
  <section>
    <section class="visit_shop">
      <div class="text">
        <h5>LOCATIONS</h5>
        <h3>Visit our Bakeries</h3>
      </div>
      <div class="container_contacts">
        <div class="contact">
          <div class="contact_img">
            <img
              src="../../assets/image/new-york-bk-600x397.jpg"
              alt="bakery"
            />
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
    <section class="social">
        <div class="square_img">
          <img src="../../assets/image/social-1.jpg" alt="social">
        </div>
        <div class="box_CTA">
          <div class="text">
            <h5>MADE FOR SHARING</h5>
            <h3>Let's stay in touch</h3>
            <button class="btn_lilac"> <span><i class="fab fa-instagram"></i></span>
              Follow us</button>
          </div>
        </div>
        <div class="square_img">
          <img src="../../assets/image/social-2.jpg" alt="social">
        </div>
    </section>
    <div class="social">
      <div class="square_img"><img src="../../assets/image/social-3.jpg" alt="social"></div>
      <div class="square_img"><img src="../../assets/image/social-4.jpg" alt="social"></div>
      <div class="square_img"><img src="../../assets/image/social-5.jpg" alt="social"></div>
      <div class="square_img"><img src="../../assets/image/social-6.jpg" alt="social"></div>
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
.visit_shop {
  @include margin_top_bottom_70px;
  @include container_80;
  @include section_header;
  margin-bottom: 4.375rem;
  .text {
    text-align: center;
  }
  .container_contacts {
    justify-content: space-between;
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

        p {
          padding: 0.1875rem 0;
        }
      }
    }
  }
}
.social {
  width: 100%;
  height: 250px;
  display: flex;
  @include margin_top_bottom_70px;
  @include container_80;
  @include section_header;
  margin-bottom: 10px;
 
    .square_img {
      margin: 0 10px;
      width: calc(25% - 20px);
      height: 100%;
      overflow: hidden;
        img{
          width: 100%;
          object-fit: cover;
        }
     
      
      
   
    }
    .box_CTA {
      display: flex;
      justify-content: center;
      align-items: center;
      margin: 0 10px;
      width: calc(50% - 20px);
      height: 100%;
      background-color: $main_color_light;
        .text{
          text-align: center;
        }
        button span{
          margin-right: .25rem;
        }
      
 
    }

}
</style>