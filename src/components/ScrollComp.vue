<template>
    <div class="square position-fixed" @click="scrollToTop" ref="showButton">
        <i class="fa-solid fa-chevron-up"></i>
    </div>
</template>

<script>
import { store } from '../store';
export default {
    name: 'ScrollTop',
    data() {
        return {
            store,
        }
    },
    methods: {
        scrollToTop() {
            window.scrollTo({
                top: 0,
            });
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/variables' as *;

.square {
    bottom: 3%;
    right: 5%;
    z-index: 100;
    background-color: $primary;
    color: $text-opacity;
    padding: 1.1em 1.3em;
    border-radius: 50%;
    cursor: pointer;
}
</style>