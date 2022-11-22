<template>
    <div class="container-fluid d-flex justify-content-between">
        <div class="mycontainer col-lg-5 col-md-12 col-sm-12">
            <p class="pre-title">Our products</p>
            <h1>All our delectable pastries are backed fresh in our Kitchen very morning, and are made with all-natural,
                all
                organic ingredients.</h1>
            <button class="mybutton">Start shopping</button>
        </div>
        <div class="carousel mycontainer">
            <div class="mycarousel" ref="scroll">
                <div class="slider-wrapper">
                    <div class="slide text-center" v-for="(slide, index) in slides" :key="index">
                        <img :src="slide.img" :alt="slide.name">
                        <!-- <p class="text-capitalize">{{ slide.name }}</p>
                        <span>{{ slide.price }}</span> -->
                    </div>
                </div>

                <!-- <div class="overlay-card">
                                <p>ciao</p>
                            </div> -->
            </div>
            <span @click="scrollLeft"><i class="fa-solid fa-chevron-left"></i></span>
            <span @click="scrollRight"><i class="fa-solid fa-chevron-right"></i></span>
        </div>
    </div>


</template>

<script>
export default {
    name: 'CarouselComp',
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
            ]
        }
    },
    methods: {
        scrollLeft() {
            this.$refs['scroll'].scrollLeft -= 800;
            console.log(this.$refs['scroll'].scrollLeft, 'sono fuori if');
            // if (this.$refs['scroll'].scrollLeft === 0) {
            //     this.$refs['scroll'].scrollLeft += 1100;
            //     console.log(this.$refs['scroll'].scrollLeft);
            // }
        },
        scrollRight() {
            this.$refs['scroll'].scrollLeft += 800;
            console.log(this.$refs['scroll'].scrollLeft);
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/general.scss' as *;

//     // .overlay-card {
//     //     position: absolute;
//     //     top: 0;
//     //     bottom: 0;
//     //     left: 0;
//     //     right: 0;
//     //     z-index: 5;
//     //     background-color: rgba(0, 0, 0, 0.171);
//     // }
// }

// // .carousel-control-prev,
// // .carousel-control-next {
// //     width: 5%;
// // }

// // .carousel-control-prev-icon,
// // .carousel-control-next-icon {
// //     background-color: $primary;
// //     padding: 50px 0;
// // }

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

        // .overlay-card {
        //     position: absolute;
        //     top: 0;
        //     bottom: 0;
        //     left: 0;
        //     right: 0;
        //     z-index: 5;
        //     background-color: rgba(0, 0, 0, 0.171);
        // }
        .slider-wrapper {
            width: 1575px;
            display: flex;
            flex-flow: row;
            gap: 1em;
            position: relative;

            .slide img {
                width: 380px;
                height: 480px;
            }
        }
    }
}
</style>