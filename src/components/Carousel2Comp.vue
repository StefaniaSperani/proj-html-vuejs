<template>
    <div class="container-fluid d-flex justify-content-between">
        <div class="mycontainer text-center col-lg-5 col-md-12 col-sm-12">
            <h1>Find a freshly baked product perfect for you</h1>
            <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Consectetur quasi rem minus pariatur iusto
                veniam. Nemo, dignissimos. </p>
            <button class="mybutton">Start all products</button>
        </div>
        <div class="carousel mycontainer">
            <div class="carousel slide">
                <div class="carousel-inner">
                    <div class="carousel-item active">
                        <div class="mycarousel ">
                            <img src="public\images\choco-chip-cookies.jpg" alt="Choco-Chip">
                            <!-- <p>Choco chip cookies</p>
                            <span>$19.00 - $39.00</span> -->
                            <img src="public\images\strawberry-jam-cookies.jpg" alt="Jam-Coockies">
                            <img src="public\images\choco-chip-cookies.jpg" alt="Choco-Chip">
                            <img src="public\images\strawberry-jam-cookies.jpg" alt="Jam-Coockies">
                            <!-- <div class="overlay-card">
                                <p>ciao</p>
                            </div> -->
                        </div>

                    </div>
                </div>
                <button class="carousel-control-prev" type="button">
                    <span><i class="fa-solid fa-chevron-left"></i></span>
                </button>
                <button class="carousel-control-next" type="button">
                    <span><i class="fa-solid fa-chevron-right"></i></span>
                </button>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'Carousel2Comp'
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/general.scss' as *;

.mybutton {
    text-transform: capitalize;
}

.mycarousel {
    display: flex;
    flex-flow: row;
    gap: 1em;
    position: relative;

    img {
        width: 24%;
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
}

.carousel-control-prev,
.carousel-control-next {
    width: 4%;
}

.fa-chevron-right,
.fa-chevron-left {

    background-color: $primary;
    padding: 20px 18px;
    width: 7px;
}
</style>