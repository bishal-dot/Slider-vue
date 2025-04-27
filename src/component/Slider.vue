<script setup>

import 'vue3-carousel/carousel.css'
import { Carousel, Slide, Pagination, Navigation } from 'vue3-carousel'


// store images in a array
const Images=[
  {
    id:1,
    image:'src/images/aizen.png',
  },
  {
    id:2,
    image:'src/images/asta.jpeg',
  },
  {
    id:3,
    image:'src/images/berserk.jpg',
  },
  {
    id:4,
    image:'src/images/hinata.png',
  },
  {
    id:5,
    image:'src/images/jjk.jpg',
  },
  {
    id:6,
    image:'src/images/killua.jpg',
  },
  {
    id:7,
    image:'src/images/law.jpg',
  },
  {
    id:8,
    image:'src/images/luffy.jpg',
  }

]
const carouselConfig = {
  itemsToShow: 1,
  wrapAround: true,
  autoplay: 3000
}


</script>

<template>
  <Carousel v-bind="carouselConfig">
    <Slide v-for="image in Images" :key="image.id">
      <div class="images">
        <img :src="image.image">
      </div>
    </Slide>
    <template #addons>
      <Navigation />
      <Pagination /> 
    </template>
  </Carousel>
</template>

<style>
    .images{
        width: 1080px;
        height: 720px;
        display: flex;
        align-items: center;
        justify-content: center;
        overflow: hidden;
        object-position: center;
        object-fit: cover;
    }
    .images img{
        width: 100%;
    }
    .carousel__icon{
      border-radius: 50%;
      background-color:springgreen;
    }
</style>