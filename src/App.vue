<template>

  <header>
    <NavbarComp />
    <JumboComp />
  </header>

  <main>
    <CarouselComp />
    <MomentsComp />
    <Carousel2Comp />

  </main>

  <footer>

  </footer>

</template>

<script>
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