<script>
import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
import FooterApp from './components/FooterApp.vue';

export default {
  components: {
    HeaderApp,
    MainApp,
    FooterApp
  }
}
</script>

<template>
  <!-- HEADER SECTION -->
  <section>
    <HeaderApp />
  </section>

  <!-- MAIN SECTION -->
  <section>
    <MainApp />
  </section>

  <!-- FOOTER SECTION -->
  <section>
    <!-- top footer section -->
    <FooterApp />
    <!-- bottom footer section -->
    <SocialFooterApp />
  </section>



</template>

<style lang="scss"></style>