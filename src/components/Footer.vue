<template>
  <footer>
    <section class="footer-hero">
      <div class="container hero">
        <div class="text">
          <h5>TRY OUR SEASONAL PRODUCTS</h5>
          <h3>Order for pick-up or delivery to your home</h3>
        </div>
        <button class="btn_white">Shop Now</button>
      </div>
    </section>
    <section class="footer-top">
      <div class="logo">
        <img src="../assets/image/avada-bakery-logo.png" alt="logo" />
      </div>
      <div>
        <h3>Subscribe to our Newsletter</h3>
        <input type="text" placeholder="Enter email address*" />
        <button class="btn_lilac">Subscribe</button>
      </div>
    </section>
    <section class="footer-nav">
      <ul>
        <li>
          <Link v-for="(link, index) in result" :key="index" :link="link" />
          <a href="#">
            <i class="fas fa-shopping-cart"></i>

            <span class="ordersNumber"> 0 </span>
          </a>
        </li>
      </ul>
    </section>
    <section class="footer-bottom">
      <div class="copyright">
        <p>
          © Copyright 2021 | Avada Theme by ThemeFusion | All Rights Reserved |
          Powered by WordPress |<span id="MK">
            replication of Maria Klimenko <span class="pulse">&#x2665;</span>
          </span>
        </p>
      </div>
      <div class="icon-social">
        <ul>
          <li>
            <a href="#">
              <i class="fab fa-instagram"></i>
            </a>
          </li>
          <li>
            <a href="#">
              <i class="fab fa-twitter"></i>
            </a>
          </li>
          <li>
            <a href="#">
              <i class="fab fa-facebook"></i>
            </a>
          </li>
          <li>
            <a href="#">
              <i class="fab fa-pinterest-p"></i>
            </a>
          </li>
        </ul>
      </div>
    </section>
  </footer>
</template>

<script>
import elm from "./Date/links.json";
import Link from "./Date/Link.vue";
export default {
  name: "Footer",
  components: {
    Link,
  },
  data() {
    return {
      links: elm,
      result: "",
    };
  },
  created() {
    this.result = this.links.slice(1);
    console.log(this.result);
  },
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
.footer-top {
  @include margin_top_bottom_70px;
  @include container_80;
  @include section_header;
  display: flex;
  justify-content: space-between;
  align-items: center;
  text-align: right;
  h3 {
    font-family: "Work Sans", sans-serif;
    font-size: 1.125rem;
  }
  input {
    padding: 0.625rem 1.375rem;
    margin-right: 0.3125rem;
    border: 1px solid rgba(196, 190, 190, 0.534);
    border-radius: 0.4375rem;
    &:hover {
      border: 1px solid rgba(182, 155, 155, 0.726);
    }
    &:focus {
      outline: none;
    }
  }
}
.footer-nav {
  font-size: 1rem;
  @include container_80;
  margin-top: 1.25rem;
  li > a {
    padding: 0.625rem 0.9375rem;
    transition: all 0.7s ease;
    &:hover {
      color: rgb(51, 21, 90);
      background-color: rgba(188, 143, 143, 0.274);
    }
  }
  .ordersNumber {
    margin-left: 0.3125rem;
    display: inline-block;
    text-align: center;
    width: 1.25rem;
    height: 1.25rem;
    line-height: 1.25rem;
    vertical-align: middle;
    border-radius: 50%;
    background-color: $main_color_light;
  }
}

.footer-bottom {
  @include container_80;
  @include margin_top_bottom_70px;
  display: flex;
  justify-content: space-between;
  .copyright {
    font-size: 14px;
  }
  .icon-social {
    a {
      padding: 0 0.625rem;
      transition: all 0.7s ease;
      &:hover {
        color: rgb(177, 15, 142);
      }
    }
  }
}

@mixin inline-animation($duration) {
  $name: inline-#{unique-id()};

  @keyframes #{$name} {
    @content;
  }

  animation-name: $name;
  animation-duration: $duration;
  animation-iteration-count: infinite;
}

.pulse {
  opacity: 0;
  font-size: 0.9375rem;
  color: rgb(209, 9, 52);
  animation: all;
  transition: all 0.7s ease;
}
.pulse {
  @include inline-animation(2s) {
    from {
      font-size: 0.75rem;
    }
    to {
      font-size: 0.875rem;
    }
  }
}

#MK {
  transition: all 0.7s ease;
}
#MK:hover {
  color: rgb(209, 9, 52);
  cursor: pointer;
  font-weight: 500;
}
#MK:hover .pulse {
  opacity: 1;
}
</style>