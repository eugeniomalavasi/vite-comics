<script>
import HeaderApp from './components/HeaderApp.vue';
import BannerApp from './components/BannerApp.vue';
import MainApp from './components/MainApp.vue';
import IconList from './components/IconList.vue';
import FooterApp from './components/FooterApp.vue';

export default {
  components: {
    HeaderApp,
    MainApp,
    FooterApp,
    IconList,
    BannerApp
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
    <BannerApp />
  </section>

  <!-- MAIN SECTION -->
  <section>
    <MainApp />
  </section>

  <!-- ICON LIST SECTION -->
  <IconList />
  
  <!-- FOOTER SECTION -->
  <section>
    <FooterApp />
  </section>



</template>

<style lang="scss"></style>