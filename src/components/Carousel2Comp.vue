<template>
    <div class="container-fluid d-flex justify-content-between">
        <div class="mycontainer text-center">
            <h1>Find a freshly baked product perfect for you</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur quasi rem minus pariatur iusto
                veniam. Nemo, dignissimos. </p>
            <button class="mybutton">Start all products</button>
        </div>
        <!-- CAROUSEL -->
        <div class="carousel mycontainer">
            <div class="mycarousel" ref="scroll">
                <div class="slider-wrapper">
                    <div class="slide text-center" v-for="(slide, index) in slides" :key="index">
                        <img :src="slide.img" :alt="slide.name">
                        <p class="text-capitalize">{{ slide.name }}</p>
                        <span>{{ slide.price }}</span>
                        <div class="overlay-card">
                            <div class="hover-text">
                                <span class="pre-title">
                                    Select options
                                </span>
                                <span class="pre-title">
                                    Quick view
                                </span>
                            </div>
                        </div>
                    </div>
                </div>
            </div>
            <span @click="scrollLeft"><i class="fa-solid fa-chevron-left"></i></span>
            <span @click="scrollRight"><i class="fa-solid fa-chevron-right"></i></span>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Carousel2Comp',
    data() {
        return {
            slides: [
                {
                    img: 'public/images/choco-chip-cookies.jpg',
                    name: 'Choco chip cookies',
                    price: '$19.00 - $39.00'
                },
                {
                    img: 'public/images/strawberry-jam-cookies.jpg',
                    name: 'Strawberry jam cookies',
                    price: '$19.00 - $39.00'
                },
                {
                    img: 'public/images/blackberry-stuffed-bread.jpg',
                    name: 'Blackberry stuffed bread',
                    price: '$19.00 - $39.00'
                },
                {
                    img: 'public/images/strawberry-donut.jpg',
                    name: 'Strawberry donut',
                    price: '$19.00 - $39.00'
                },
                {
                    img: 'public/images/perfect-macarons.jpg',
                    name: 'Macarons',
                    price: '$19.00 - $39.00'
                },
                {
                    img: 'public/images/home-bread.jpg',
                    name: 'Home bread',
                    price: '$19.00 - $39.00'
                },
                {
                    img: 'public/images/premium-bread.jpg',
                    name: 'Premium bread',
                    price: '$19.00 - $39.00'
                },
                {
                    img: 'public/images/cherry-cake.jpg',
                    name: 'Cherry cake',
                    price: '$19.00 - $39.00'
                },
                {
                    img: 'public/images/cookies-with-ice-cream.jpg',
                    name: 'Cookis ice cream',
                    price: '$19.00 - $39.00'
                },
                {
                    img: 'public/images/glazed-pancake-with-lemon.jpg',
                    name: 'Glazed pancake',
                    price: '$19.00 - $39.00'
                },
                {
                    img: 'public/images/small-cupcake.jpg',
                    name: 'Cupcake',
                    price: '$19.00 - $39.00'
                },
                {
                    img: 'public/images/premium-bread.jpg',
                    name: 'Premium bread',
                    price: '$19.00 - $39.00'
                }
            ]
        }
    },
    methods: {
        scrollLeft() {
            this.$refs['scroll'].scrollLeft -= 1100;
            // if (this.$refs['scroll'].scrollLeft === 0) {
            //     this.$refs['scroll'].scrollLeft += 1100;
            //     console.log(this.$refs['scroll'].scrollLeft);
            // }
        },
        scrollRight() {
            this.$refs['scroll'].scrollLeft += 1100;
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/general.scss' as *;

.mycontainer {
    padding: 0 !important;
    margin: 5em;
    overflow: hidden;

    .mybutton {
        text-transform: capitalize;
    }

    i {
        position: absolute;
        top: 50%;
        transform: translateY(-50%);
        background-color: $primary;
        padding: 25px 10px;
        cursor: pointer;

        &.fa-chevron-right {
            right: 0;
        }

        &.fa-chevron-left {
            left: 0;
        }
    }

    .mycarousel {
        overflow: auto;

        &::-webkit-scrollbar {
            display: none;
        }

        .slider-wrapper {
            width: 2345px;
            display: flex;
            flex-flow: row;
            gap: 1em;
            position: relative;

            .slide {
                position: relative;

                .overlay-card {
                    display: none;
                    position: absolute;
                    top: 0;
                    bottom: 0;
                    left: 0;
                    right: 0;
                    z-index: 5;
                    background-color: rgba(0, 0, 0, 0.171);
                }

                .hover-text {
                    position: absolute;
                    z-index: 5;
                    top: 50%;
                    left: 50%;
                    transform: translate(-50%, -50%);
                    color: $text-opacity;
                }


                img {
                    width: 260px;
                    height: 320px;
                }
            }

            .slide:hover .overlay-card {
                display: block;
            }
        }
    }
}
</style>