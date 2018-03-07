<template>
    <nav class="navbar navbar-default navbar-fixed-top">
        <div class="container-fluid">
            <div class="navbar-collapse mobile-burger">
                <div class="wrapper">
                    <span class="burger navbar__burger" :class="{'open': isToggle}" @click="toggleMenu">
                        <span></span>
                        <span></span>
                        <span></span>
                    </span>
                </div>
            </div>
            <div class="navbar-collapse mobile-nav" :class="{'open': isToggle}">
                <div class="wrapper">
                    <ul class="nav navbar-nav">
                        <nuxt-link tag="li" to="/" active-class="active" exact>
                            <a href="javascript: void(0);">home</a>
                        </nuxt-link>
                        <nuxt-link tag="li" to="/about" active-class="active" exact>
                            <a href="javascript: void(0);">about</a>
                        </nuxt-link>
                        <nuxt-link tag="li" to="/contact-us" active-class="active" exact>
                            <a href="javascript: void(0);">contact us</a>
                        </nuxt-link>
                    </ul>
                </div>
            </div>
        </div>
    </nav>
</template>

<script>
  export default {
    name: 'menu-nav',
    data () {
      return {
        isToggle: false,
      }
    },
    methods: {
      toggleMenu () {
        this.isToggle = !this.isToggle
      },
    },
  }
</script>

<style lang="stylus">
    .burger {
        width: 50px;
        height: 35px;
        position: relative;
        margin: 7px 0;
        -webkit-transform: rotate(0deg);
        -moz-transform: rotate(0deg);
        -o-transform: rotate(0deg);
        transform: rotate(0deg);
        -webkit-transition: .5s ease-in-out;
        -moz-transition: .5s ease-in-out;
        -o-transition: .5s ease-in-out;
        transition: .5s ease-in-out;
        cursor: pointer;
        display: block;
        -webkit-transform: scale(.7, .7);
        -moz-transform: scale(.7, .7);
        -ms-transform: scale(.7, .7);
        -o-transform: scale(.7, .7);
        transform: scale(.7, .7);
    }

    .burger span {
        display: block;
        position: absolute;
        height: 5px;
        width: 100%;
        background: #979ca3;
        //background-color : #979ca3;
        border-radius: 5px;
        opacity: 1;
        left: 0;
        -webkit-transform: rotate(0deg);
        -moz-transform: rotate(0deg);
        -o-transform: rotate(0deg);
        transform: rotate(0deg);
        -webkit-transition: .25s ease-in-out;
        -moz-transition: .25s ease-in-out;
        -o-transition: .25s ease-in-out;
        transition: .25s ease-in-out;
    }

    .burger span:nth-child(1) {
        top: 0px;
    }

    .burger span:nth-child(2) {
        top: 13px;
    }

    .burger span:nth-child(3) {
        top: 26px;
    }

    .burger.open span:nth-child(1) {
        top: 13px;
        -webkit-transform: rotate(135deg);
        -moz-transform: rotate(135deg);
        -o-transform: rotate(135deg);
        transform: rotate(135deg);
    }

    .burger.open span:nth-child(2) {
        opacity: 0;
        left: -60px;
    }

    .burger.open span:nth-child(3) {
        top: 13px;
        -webkit-transform: rotate(-135deg);
        -moz-transform: rotate(-135deg);
        -o-transform: rotate(-135deg);
        transform: rotate(-135deg);
    }

    .burger.open span {
        // background-color: blue;
    }

    .mobile-burger {
        display: none
        background-color: #f8f8f8;
        border-color: #e7e7e7;
        position: relative
        z-index: 1
    }

    .container-fluid {
        position: relative
    }

    @media screen and (max-width: 768px) {
        .navbar-fixed-top .navbar-collapse {
            max-height: 50px;
        }

        .nav {
            background-color: #f8f8f8;
            border-color: #e7e7e7;
            margin-top: 0;
            margin-bottom: 0
        }

        .mobile-nav {
            position: absolute
            width: 100%
            z-index: -1
            -webkit-transform: translate(0, -200px)
            -moz-transform: translate(0, -200px)
            -ms-transform: translate(0, -200px)
            -o-transform: translate(0, -200px)
            transform: translate(0, -200px)
            -webkit-transition: all .3s
            -moz-transition: all .3s
            -ms-transition: all .3s
            -o-transition: all .3s
            transition: all .3s
            max-height: 0 !important
            &.open {
                -webkit-transform: translate(0, 0)
                -moz-transform: translate(0, 0)
                -ms-transform: translate(0, 0)
                -o-transform: translate(0, 0)
                transform: translate(0, 0)
            }
        }

        .mobile-burger {
            display: block
        }
    }
</style>