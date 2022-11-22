<template>
    <div class="container-fluid">
        <div class="mycontainer d-flex justify-content-between">
            <div class="left">
                <a href="#"><img src="public\images\avada-bakery-logo-retina-200x97.png" alt="Logo"></a>
                <ul class="navbar-nav d-flex flex-row pt-4">
                    <li class="nav-item" v-for="(link, index) in links" :key="index">
                        <a :href="link.url" :class="{ 'active': link.current }">{{ link.text }}</a>
                    </li>
                    <li><a href="#"><i class="fa-solid fa-cart-shopping"></i> <span class="cart">0</span></a></li>
                </ul>
            </div>

            <div class="right justify-content-end flex-column">
                <h2>Subscribe to our Newsletter</h2>

                <input type="email" placeholder="Enter email adress*" class="mx-4">
                <button class="mybutton">Subscribe</button>
            </div>
        </div>
        <div class="mycontainer bottom d-flex justify-content-between">
            <p class="pre-title text-capitalize">&#169; Copyright 2012 - 2020 | aAvada theme by ThemeFusion | All right
                reserved | Powered by WordPress</p>

            <div class="social-icons">
                <i class="fa-brands fa-instagram"></i>
                <i class="fa-brands fa-twitter"></i>
                <i class="fa-brands fa-facebook-f"></i>
                <i class="fa-brands fa-pinterest"></i>
            </div>
        </div>

    </div>
</template>

<script>
import { store } from '../store'
export default {
    name: 'FooterComp',
    data() {
        return {
            store,
            links: [
                {
                    text: "Shop",
                    url: "#",
                    current: false,
                },
                {
                    text: "About",
                    url: "#",
                    current: false,
                },
                {
                    text: "Gallery",
                    url: "#",
                    current: false,
                },
                {
                    text: "Locations",
                    url: "#",
                    current: false,
                },
                {
                    text: "Journal",
                    url: "#",
                    current: false,
                },
                {
                    text: "Contact",
                    url: "#",
                    current: false,
                },
                {
                    text: "Orders",
                    url: "#",
                    current: false,
                },
            ],
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/variables' as *;

ul {
    list-style: none;

    li a {
        text-transform: capitalize;
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

    .cart {
        padding: 0.3em;
        background-color: $bg-section;
        width: 50px;
        height: 50px;
        border-radius: 50%;
    }

}

input {
    padding: 0.7em;
    border: 1px solid $bg-section;
    border-radius: 10px;

    &:focus-visible {
        outline: 1px solid $light-purple;
    }


}

.fa-brands {
    color: $primary;
    font-size: 30px;
    margin-left: 2em;
    cursor: pointer;
}
</style>