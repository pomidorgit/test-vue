<template>
    <div>
        <header class="header">
            <menu-nav/>
        </header>
        <nuxt/>
    </div>
</template>

<script>
  import menuNav from '~/components/menu';

  export default {
    components: {menuNav},

  };
</script>

<style>
    html {
        font-family: 'Roboto', sans-serif;
        font-size: 16px;
        word-spacing: 1px;
        -ms-text-size-adjust: 100%;
        -webkit-text-size-adjust: 100%;
        -moz-osx-font-smoothing: grayscale;
        -webkit-font-smoothing: antialiased;
        box-sizing: border-box;
    }

    *, *:before, *:after {
        box-sizing: border-box;
        margin: 0;
    }

    .button--green {
        display: inline-block;
        border-radius: 4px;
        border: 1px solid #3b8070;
        color: #3b8070;
        text-decoration: none;
        padding: 10px 30px;
    }

    .button--green:hover {
        color: #fff;
        background-color: #3b8070;
    }

    .button--grey {
        display: inline-block;
        border-radius: 4px;
        border: 1px solid #35495e;
        color: #35495e;
        text-decoration: none;
        padding: 10px 30px;
        margin-left: 15px;
    }

    .button--grey:hover {
        color: #fff;
        background-color: #35495e;
    }
    .header{
        background-color: #ccc;
    }
    .wrapper{
        max-width: 1000px;
        margin: 0 auto;
    }
    .container {
        min-height: 150vh;
        padding-top: 160px;
    }

    .title {
        text-align: center;
        font-size: 50px;
    }

    .subtitle {
        font-weight: 300;
        font-size: 42px;
        color: #526488;
        word-spacing: 5px;
        padding-bottom: 15px;
    }

    .links {
        padding-top: 15px;
    }
    .carousel__item{
        padding: 0 5px;
    }
    .carousel__item img{
        width: 100%;
    }
</style>
