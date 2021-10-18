<template>
  <section>
  <vueper-slides
  class="no-shadow"
  :visible-slides="4"
  slide-multiple
  :gap="1"
  :slide-ratio="1 / 3"
  :dragging-distance="200"
 
  :breakpoints="{ 800: { visibleSlides: 2, slideMultiple: 2 } }">

  

  <vueper-slide v-for="(slide,i) in  slides" :key="i" :image="slide.content" :title="slide.title"
   />


</vueper-slides>
  </section>
</template>

<script>
import { VueperSlides, VueperSlide } from "vueperslides";
import "vueperslides/dist/vueperslides.css";
export default {
  components: { VueperSlides, VueperSlide },
  data: () => ({
  slides: [
    {
      title: 'Slide #1',
      content: require("../../assets/image/choco-chip-cookies-400x510.jpg")
    },
     {
      title: 'Slide #2',
      content: require("../../assets/image/strawberry-jam-cookies-400x510.jpg")
    },
     {
      title: 'Slide #3',
      content: require("../../assets/image/strawberry-donut-400x510.jpg")
    },
     {
      title: 'Slide #4',
      content: require("../../assets/image/perfect-macarons-400x510.jpg")
    },
     {
      title: 'Slide #5',
      content: require("../../assets/image/choco-chip-cookies-400x510.jpg")
    },
     {
      title: 'Slide #6',
      content: require("../../assets/image/choco-chip-cookies-400x510.jpg")
    },
     {
      title: 'Slide #7',
      content: require("../../assets/image/choco-chip-cookies-400x510.jpg")
    },
   
  ]
})
};

</script>

<style lang="scss">
.vueperslide::before{
  content: attr(title);
   position: absolute;
        display: flex;
        justify-content: center;
        align-items: center;
        top: 0;
        bottom: 0;
        right: 0;
        left: 0;
        background-color: rgba(39, 33, 33, 0.39);
        // opacity: 0;
        transition: all 1s;
        cursor: pointer;
        
}

.vueperslide:hover{
  border: 4px solid rgb(217, 255, 0);
}

</style>