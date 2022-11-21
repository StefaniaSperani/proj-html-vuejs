<template>
    <nav class="navbar navbar-expand-lg">
        <div class="container-fluid">
            <a href="#"><img src="public\images\avada-bakery-logo-retina-200x97.png" alt="Logo"></a>
            <button class="navbar-toggler" type="button" aria-label="Toggle navigation">
                <span class="navbar-toggler-icon"></span>
            </button>
            <div class="collapse navbar-collapse justify-content-end">
                <ul class="navbar-nav">
                    <li class="nav-item" v-for="(link, index) in store.links" :key="index">
                        <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
                    </li>
                    <li><a href="#"><i class="fa-solid fa-cart-shopping"></i></a></li>
                </ul>
            </div>
        </div>
    </nav>
</template>

<script>
import { store } from '../store';

export default {
    name: 'NavbarComp',
    data() {
        return {
            store,
        }
    },
}
</script>

<style lang="scss" scoped>
@import '../assets/partials/variables';

nav {
    position: fixed;
    top: 0;
    left: 0;
    z-index: 10;
    width: 100%;
    height: 90px;
    padding: 0.7em;
    background-color: $bg-section;
    font-size: 0.9em;


    img {
        width: 170px;
    }

    ul {
        list-style: none;

        li a {
            text-transform: uppercase;
            text-decoration: none;
            margin: 1em;
            padding-bottom: 0.3em;
            color: $primary;

            &.active,
            &:hover {
                border-bottom: 3px solid $primary;
                transition: 0.3s;
            }
        }

    }
}
</style>