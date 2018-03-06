<template>
    <section class="container">
        <h1 class="title">{{ titlePages }}</h1>

        <slick class="carousel" ref="slick" :options="slickOptions">
            <a class="carousel__item" href="#">
                <img src="https://picsum.photos/200/300/?random=654" alt="">
                <span>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cupiditate deleniti dolore est, id magnam optio praesentium reiciendis reprehenderit sequi vel.</span>
            </a>
            <a class="carousel__item" href="#">
                <img src="https://picsum.photos/200/300/?random=65" alt="">
                <span>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cupiditate deleniti dolore est, id magnam optio praesentium reiciendis reprehenderit sequi vel.</span>
            </a>
            <a class="carousel__item" href="#">
                <img src="https://picsum.photos/200/300/?random=6" alt="">
                <span>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cupiditate deleniti dolore est, id magnam optio praesentium reiciendis reprehenderit sequi vel.</span>
            </a>
            <a class="carousel__item" href="#">
                <img src="https://picsum.photos/200/300/?random=64" alt="">
                <span>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cupiditate deleniti dolore est, id magnam optio praesentium reiciendis reprehenderit sequi vel.</span>
            </a>
            <a class="carousel__item" href="#">
                <img src="https://picsum.photos/200/300/?random=4" alt="">
                <span>Lorem ipsum dolor sit amet, consectetur adipisicing elit. Cupiditate deleniti dolore est, id magnam optio praesentium reiciendis reprehenderit sequi vel.</span>
            </a>
        </slick>


    </section>
</template>

<script>

  import Slick from 'vue-slick';

  export default {
    head: {
      titleTemplate: 'Home',
    },
    data() {
      return {
        titlePages: 'Home',
        slickOptions: {
          dots: true,
          infinite: true,
          slidesToShow: 3,
          responsive: [
            {
              breakpoint: 1024,
              settings: {
                slidesToShow: 3,
                slidesToScroll: 3,
              }
            },
            {
              breakpoint: 800,
              settings: {
                slidesToShow: 2,
                slidesToScroll: 2
              }
            },
            {
              breakpoint: 480,
              settings: {
                slidesToShow: 1,
                slidesToScroll: 1
              }
            }
        ]
        },
      };
    },
    components: { Slick }
  };
</script>
