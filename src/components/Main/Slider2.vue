<template>
 
    <vueper-slides
      class="no-shadow"
      :visible-slides="2"
      slide-multiple
      :gap="1"
      :slide-ratio="1 / 2"
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