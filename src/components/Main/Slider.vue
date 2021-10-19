<template>
 
    <vueper-slides
      class="no-shadow"
      :visible-slides="2"
      slide-multiple
      :gap="1"
      :slide-ratio="1 / 3"
      :dragging-distance="200"
      :breakpoints="{ 800: { visibleSlides: 2, slideMultiple: 2 } }"
    >
      <vueper-slide
        v-for="(slide, i) in slides"
        :key="i"
        :image="slide.content"
        :title="slide.title"
        :content="slide.price"
      />
      
    </vueper-slides>
    

</template>
<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";
export default {
  components: { VueperSlides, VueperSlide },
  data: () => ({
    slides: [
      {
        title: "Choco Chip Cookies",
        content: require("../../assets/image/choco-chip-cookies-400x510.jpg"),
        price: "$18.00 – $32.00",
        type: "Coocies, Pastries",
      },
      {
        title: "Strawberry Jam Cookies",
        content: require("../../assets/image/strawberry-jam-cookies-400x510.jpg"),
        price: "$18.00 – $32.00",
        type: "Coocies, Pastries",
      },
      {
        title: "Strawberry Donut",
        content: require("../../assets/image/strawberry-donut-400x510.jpg"),
        price: "$18.00 – $32.00",
        type: "Coocies, Pastries",
      },
      {
        title: "Perfect Macarons",
        content: require("../../assets/image/perfect-macarons-400x510.jpg"),
        price: "$18.00 – $32.00",
        type: "Coocies, Pastries",
      },
      {
        title: "Choco Chip Cookies",
        content: require("../../assets/image/choco-chip-cookies-400x510.jpg"),
        price: "$18.00 – $32.00",
        type: "Coocies, Pastries",
      },
      {
        title: "Strawberry Jam Cookies",
        content: require("../../assets/image/strawberry-jam-cookies-400x510.jpg"),
        price: "$18.00 – $32.00",
        type: "Coocies, Pastries",
      },
      {
        title: "Strawberry Donut",
        content: require("../../assets/image/strawberry-donut-400x510.jpg"),
        price: "$18.00 – $32.00",
        type: "Coocies, Pastries",
      },
      {
        title: "Perfect Macarons",
        content: require("../../assets/image/perfect-macarons-400x510.jpg"),
        price: "$18.00 – $32.00",
        type: "Coocies, Pastries",
      },
    ],
  }),
};
</script>

<style lang="scss" >
.vueperslide {
  color: rgba(255, 255, 255, 0);
  font-size: 1.5625rem;
  font-weight:600;
  transition: all 1s;

}

.vueperslide__title, .vueperslide__content{

opacity: 0;
transition: all 1s;
background-color: rgba(16, 17, 17, 0.39);
width: 100%;
padding: .9375rem 0;
}

// .vueperslide::after {
//   content: "";
//   display: flex;
//   position: absolute;
//   justify-content: center;
//   align-items: center;
//   top: 0;
//   bottom: 0;
//   right: 0;
//   left: 0;
//   background-color: rgba(39, 33, 33, 0.39);
//   opacity: 1;
//   transition: all 1s;
//   cursor: pointer;
// }


// <div target="_self" aria-hidden="false" class="vueperslide vueperslide--active vueperslide--visible" style="background-image: url(&quot;img/choco-chip-cookies-400x510.a12500a7.jpg&quot;); width: 49.5%; margin-right: 1%;"><!----><!----><div class="vueperslide__content-wrapper"><div class="vueperslide__title">Choco Chip Cookies</div><div class="vueperslide__content">$18.00 – $32.00</div></div><!----></div>

.vueperslide:hover .vueperslide__title {
 opacity: 1;
 color: rgb(255, 255, 255);

}
.vueperslide:hover .vueperslide__content {
 opacity: 1;
 color: rgb(255, 255, 255);
}

.vueperslide:hover{
  filter: brightness(87%);
  opacity: 1;
}
</style>