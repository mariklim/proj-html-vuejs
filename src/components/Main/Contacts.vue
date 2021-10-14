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
            <h3>London</h3>
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
    <section class="row">
      <div class="square_img">
        <img src="../../assets/image/social-1.jpg" alt="social" />
      </div>
      <div class="box_CTA">
        <div class="text">
          <h5>MADE FOR SHARING</h5>
          <h3>Let's stay in touch</h3>
          <button class="btn_lilac">
            <span><i class="fab fa-instagram"></i></span> Follow us
          </button>
        </div>
      </div>
      <div class="square_img">
        <img src="../../assets/image/social-2.jpg" alt="social" />
      </div>
    </section>
    <div class="row">
      <div class="square_img">
        <img src="../../assets/image/social-3.jpg" alt="social" />
      </div>
      <div class="square_img">
        <img src="../../assets/image/social-4.jpg" alt="social" />
      </div>
      <div class="square_img">
        <img src="../../assets/image/social-5.jpg" alt="social" />
      </div>
      <div class="square_img">
        <img src="../../assets/image/social-6.jpg" alt="social" />
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
    .contact {
        flex-grow: 1;
        overflow: hidden;
      .contact_img img {
        width: 100%;
        transition: all 0.7s ease;

      }

      //hover per img di contatti
      .contact_img img:hover {
        transform: scale(1.06);
      }
    }

    .adress {
      text-align: center;
      overflow: hidden;
      z-index: 1;
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
.row {
  width: 100%;
  height: 250px;
  display: flex;
  @include margin_top_bottom_70px;
  @include container_80;
  @include section_header;
  margin-bottom: 1.25rem;

  .square_img {
    width: calc(25%);
    height: 100%;
    overflow: hidden;
    img {
      width: 100%;
      transition: all 0.7s ease;
    }
  }

  //hover per immagini di social
  .square_img img:hover {
    transform: scale(1.2);
  }

  .square_img:not(:last-child),
  .box_CTA {
    margin-right: 1.25rem;
  }
  .box_CTA {
    display: flex;
    justify-content: center;
    align-items: center;
    width: calc(50%);
    height: 100%;
    background-color: $main_color_light;
    .text {
      text-align: center;
    }
    button span {
      margin-right: 0.25rem;
    }
  }
}
</style>