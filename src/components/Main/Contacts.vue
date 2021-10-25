<template>
  <section>
    <section v-scroll-reveal.reset="{ delay: 100 }" class="visit_shop">
      <div class="text">
        <h5>LOCATIONS</h5>
        <h3>Visit our Bakeries</h3>
      </div>
      <div v-scroll-reveal.reset="{ delay: 150 }" class="container_contacts">
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
              <div class="map_NY" :class="{ active: isActivNY }">
                  <div class="btn-close" @click="
                  {
                    isActivNY = !isActivNY;
                  }
                ">
                    <i class="far fa-window-close"></i>
                  </div>
                  <h3>New York Bakery</h3>
                <iframe
                  src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d96859.65413064092!2d-73.946843!3d40.654924!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x89c25b6617a81121%3A0x9d5cc54407bdb5fa!2s775%20New%20York%20Ave%2C%20Brooklyn%2C%20NY%2011203!5e0!3m2!1sen!2sus!4v1635092174631!5m2!1sen!2sus"
                  width="500"
                  height="350"
                  style="border: 0"
                  allowfullscreen=""
                  loading="lazy"
                >
                </iframe>
              </div>
              <button
                @click="
                  {
                    isActivNY = !isActivNY;
                  }
                "
                class="btn_white"
              >
                View Map
              </button>
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
              <div class="map_London" :class="{ active: isActivLO }">
                 <div class="btn-close" @click="
                  {
                    isActivLO = !isActivLO;
                  }
                ">
                    <i class="far fa-window-close"></i>
                  </div>
                <h3>London Bakery</h3>
                <iframe
                  src="https://www.google.com/maps/embed?pb=!1m14!1m8!1m3!1d79461.6128090517!2d-0.135002!3d51.50999800000001!3m2!1i1024!2i768!4f13.1!3m3!1m2!1s0x487604d3ff201fc1%3A0xf08adf0cfb3eb2fe!2sPiccadilly%20Circus%2C%20London%2C%20UK!5e0!3m2!1sen!2sus!4v1635145591977!5m2!1sen!2sus"
                  width="500"
                  height="350"
                  style="border: 0"
                  allowfullscreen=""
                  loading="lazy"
                ></iframe>
              </div>

              <button
                class="btn_white"
                @click="
                  {
                    isActivLO = !isActivLO;
                  }
                "
              >
                View Map
              </button>
            </div>
          </div>
        </div>
      </div>
    </section>
    <section v-scroll-reveal.reset="{ delay: 100 }">
      <div class="row">
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
      </div>
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
  </section>
</template>

<script>
export default {
  name: "Contacts",
  data() {
    return {
      isActivLO: false,
      isActivNY: false,
    };
  },
};
</script>

<style lang="scss" scoped>
@import "../../assets/style/common";
@import "../../assets/style/variables";
.visit_shop {
  @include margin_top_bottom_70px;
  @include container_80;
  @include section_header;
  position: relative;
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
        .map_London, .map_NY {
          z-index: 10;
          width: 42%;
          padding-bottom: .9375rem;
          display: none;
          position: absolute;
          margin-left: auto;
          margin-right: auto;
          left: 0;
          right: 0;
          bottom: 22%;
          box-shadow: .3125rem .3125rem .9375rem .3125rem #000000;
          background-color: rgb(255, 255, 255);
        }

         .map_London.active,  .map_NY.active{
            display: inline-block;
          }

          .btn-close{
            text-align: right;
            color: rgba(133, 130, 130, 0.856);
            cursor: pointer;
          }
       
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