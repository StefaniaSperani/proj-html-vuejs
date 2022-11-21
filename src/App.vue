<template>

  <header>
    <NavbarComp />
    <JumboComp />
  </header>

  <main>

  </main>

  <footer>

  </footer>

</template>

<script>
import JumboComp from './components/JumboComp.vue';
import NavbarComp from './components/NavbarComp.vue';
import { store } from './store';

export default {
  components: {
    NavbarComp,
    JumboComp
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