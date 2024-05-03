<script>
import HeaderApp from './components/HeaderApp.vue';
import MainApp from './components/MainApp.vue';
import FooterApp from './components/FooterApp.vue';
import IconList from './components/IconList.vue';

export default {
  components: {
    HeaderApp,
    MainApp,
    FooterApp,
    IconList
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

  <!-- ICON LIST SECTION -->
  <IconList />
  
  <!-- FOOTER SECTION -->
  <section>
    <FooterApp />
  </section>



</template>

<style lang="scss"></style>