<template>
    <div class="container-fluid d-flex justify-content-between">
        <div class="mycontainer col-lg-5 col-md-12 col-sm-12">
            <p class="pre-title">Our products</p>
            <h1>All our delectable pastries are backed fresh in our Kitchen very morning, and are made with all-natural,
                all
                organic ingredients.</h1>
            <button class="mybutton">Start shopping</button>
        </div>
        <div class="carousel mycontainer col-lg-6 col-md-12 col-sm-12">
            <div class="carousel slide">
                <div class="carousel-inner">
                    <div class="carousel-item active">
                        <div class="mycarousel">
                            <img src="public\images\choco-chip-cookies.jpg" alt="Choco-Chip">
                            <img src="public\images\strawberry-jam-cookies.jpg" alt="Jam-Coockies">
                            <img src="public\images\strawberry-jam-cookies.jpg" alt="Jam-Coockies">
                            <!-- <div class="overlay-card">
                                <p>ciao</p>
                            </div> -->
                        </div>

                    </div>
                </div>
                <button class="carousel-control-prev" type="button">
                    <span class="carousel-control-prev-icon"></span>
                </button>
                <button class="carousel-control-next" type="button">
                    <span class="carousel-control-next-icon"></span>
                </button>
            </div>
        </div>
    </div>


</template>

<script>
export default {
    name: 'CarouselComp'
}
</script>

<style lang="scss" scoped>
@use '../assets/styles/general.scss' as *;

.mybutton {
    text-transform: capitalize;
}

.mycarousel {
    display: flex;
    flex-direction: row;
    gap: 1em;
    position: relative;

    img {
        width: 50%;
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
    width: 5%;
}

.carousel-control-prev-icon,
.carousel-control-next-icon {
    background-color: $primary;
    padding: 50px 0;
}
</style>