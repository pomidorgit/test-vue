<template>
    <nav class="navbar navbar-default navbar-fixed-top">
        <div class="container-fluid">
            <div class="navbar-collapse">
                <div class="wrapper">
                    <ul class="nav navbar-nav">
                        <nuxt-link tag="li" to="/" active-class="active" exact>
                            <a href="javascript: void(0);">home</a>
                        </nuxt-link>
                        <nuxt-link tag="li" to="/about" active-class="active" exact>
                            <a href="javascript: void(0);">about</a>
                        </nuxt-link>
                        <nuxt-link tag="li" to="/us-and" active-class="active" exact>
                            <a href="javascript: void(0);">us and</a>
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
  };
</script>

<style lang="stylus">

</style>