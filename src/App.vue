<template>

  <header>
    <NavbarComp />
    <JumboComp />
  </header>

  <main>
    <CarouselComp />
    <MomentsComp />
    <Carousel2Comp />
    <InfoComp />
    <StoresComp />
    <SocialComp />
    <ShopComp />
  </main>

  <footer>
    <FooterComp />
  </footer>

  <ScrollComp />
</template>

<script>
import ScrollComp from './components/ScrollComp.vue';
import FooterComp from './components/FooterComp.vue';
import ShopComp from './components/ShopComp.vue';
import SocialComp from './components/SocialComp.vue';
import StoresComp from './components/StoresComp.vue';
import InfoComp from './components/InfoComp.vue';
import Carousel2Comp from './components/Carousel2Comp.vue';
import MomentsComp from './components/MomentsComp.vue'
import CarouselComp from './components/CarouselComp.vue';
import JumboComp from './components/JumboComp.vue';
import NavbarComp from './components/NavbarComp.vue';
import { store } from './store';



export default {
  components: {
    NavbarComp,
    JumboComp,
    CarouselComp,
    MomentsComp,
    Carousel2Comp,
    InfoComp,
    StoresComp,
    SocialComp,
    ShopComp,
    FooterComp,
    ScrollComp
  },
  data() {
    return {
      store,
    }
  },

}

</script>

<style lang="scss" scoped>
@import './assets/partials/variables';
</style>