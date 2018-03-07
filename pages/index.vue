<template>
    <section class="container">
        <h1 class="title">{{ titlePages }}</h1>

        <slick class="carousel" ref="slick" :options="slickOptions">
            <a class="carousel__item" href="#">
                <img src="https://picsum.photos/200/300/?random=654" alt="">
            </a>
            <a class="carousel__item" href="#">
                <img src="https://picsum.photos/200/300/?random=65" alt="">
            </a>
            <a class="carousel__item" href="#">
                <img src="https://picsum.photos/200/300/?random=6" alt="">
            </a>
            <a class="carousel__item" href="#">
                <img src="https://picsum.photos/200/300/?random=64" alt="">
            </a>
            <a class="carousel__item" href="#">
                <img src="https://picsum.photos/200/300/?random=4" alt="">
            </a>
        </slick>


    </section>
</template>

<script>
  import Slick from 'vue-slick'

  export default {
    head: {
      titleTemplate: 'Home',
    },
    data () {
      return {
        titlePages: 'Home',
        slickOptions: {
          dots: true,
          infinite: true,
          prevArrow: '<i class="slick-prev fa fa-chevron-circle-left"></i>',
          nextArrow: '<i class="slick-next fa fa-chevron-circle-right"></i>',
          slidesToShow: 3,
          responsive: [
            {
              breakpoint: 1024,
              settings: {
                slidesToShow: 3,
                slidesToScroll: 3,
              },
            },
            {
              breakpoint: 800,
              settings: {
                slidesToShow: 2,
                slidesToScroll: 2,
                arrows: false,
              },
            },
            {
              breakpoint: 480,
              settings: {
                slidesToShow: 1,
                slidesToScroll: 1,
                arrows: false,
              },
            },
          ],
        },
      }
    },
    components: {Slick},
  }
</script>
<style lang="stylus">
    .slick-prev,
    .slick-next {
        &:before {
            color: #000;
            font-size: 25px
        }
    }
</style>
