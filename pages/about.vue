<template>
    <section class="container">

        <h1 class="title">{{ titlePages }}</h1>

    </section>
</template>

<script>
  export default {
    head:{
      titleTemplate: 'About',
    },
    data() {
      return {
        titlePages: 'About'
      }
    }
  };
</script>

