<template>
   <div class="slider-box">
      <div class="slider-content">
         <Splide :options="options" aria-label="My Favorite Images">
            <SplideSlide>
               <img src="https://theme.hstatic.net/200000411281/1000949882/14/home_slider_image_2.jpg?v=260" alt="Sample 1" />
            </SplideSlide>
            <SplideSlide>
               <img src="https://theme.hstatic.net/200000411281/1000949882/14/home_slider_image_4.jpg?v=260" alt="Sample 2" />

            </SplideSlide>

         </Splide>
      </div>
   </div>
</template>

<script>
import { Splide, SplideSlide } from "@splidejs/vue-splide";
import { defineComponent } from "vue";

export default defineComponent({
   components: {
      Splide,
      SplideSlide,
   },

   setup() {
      const options = {
         rewind: true,
         gap: "1rem",
         autoplay: true,
      };

      return { options };
   },
});
</script>

<style scoped>
.splide__slide img {
   width: 100%;
   /* height: 500px; */
   object-fit: cover;
   /* Bao phủ toàn bộ khung hình */
   display: block;
}



/* .content {
   margin-top: 5px;
   position: absolute;
   right: 10px;
   bottom: 20px;
   width: 400px;
   text-align: justify;
   background-color: #333;
   padding: 7px 7px 12px;
   border-radius: 3px;
   opacity: 0.85;
}

.content a {
   text-decoration: none;
   color: white;
   display: inline-block;
   line-height: 24px;
   text-transform: uppercase;
} */
</style>
