<template>

  <header>
    <NavbarComp />
    <JumboComp />
  </header>

  <main>
    <CarouselComp />
  </main>

  <footer>

  </footer>

</template>

<script>
import CarouselComp from './components/CarouselComp.vue';
import JumboComp from './components/JumboComp.vue';
import NavbarComp from './components/NavbarComp.vue';
import { store } from './store';

export default {
  components: {
    NavbarComp,
    JumboComp,
    CarouselComp
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