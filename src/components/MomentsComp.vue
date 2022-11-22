<template>
    <div class="container-fluid">
        <div class="mycontainer text-center">
            <p class="pre-title">
                Corporate & weddings
            </p>
            <h1>Baking special moments</h1>
            <div class="moments">
                <div class="up">
                    <img src="public\images\corporate-bg.jpg" alt="Corporate">
                    <div class="hover-corp">
                        <img src="public\images\corporate-hover-bg.jpg" alt="CorporateHover">
                        <div class="hover-text">
                            <p class="pre-title">
                                International bakery
                            </p>
                            <h1>Corporate events</h1>
                            <button class="mybutton">Explore more</button>
                        </div>
                    </div>
                </div>

                <div class="up">
                    <img src="public\images\wedding-bg.jpg" alt="Wedding">
                    <div class="hover-corp">
                        <img src="public\images\wedding-hover-bg.jpg" alt="WeddingHover">
                        <div class="hover-text">
                            <p class="pre-title">
                                Private dining hall
                            </p>
                            <h1>Wedding & parties</h1>
                            <button class="mybutton">Explore more</button>
                        </div>
                    </div>
                </div>

            </div>

        </div>

    </div>
</template>

<script>
export default {
    name: 'MomentsComp'
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/variables' as *;

h1 {
    text-transform: capitalize;
}

.moments {
    display: flex;
    justify-content: space-between;

    .up {
        position: relative;
        transition: 0.5s;
    }

    .hover-corp {
        display: none;
        position: absolute;
        top: 0;
        bottom: 0;
        left: 0;
        right: 0;


        .hover-text {
            position: absolute;
            z-index: 5;
            top: 50%;
            left: 50%;
            transform: translate(-50%, -50%);
        }

        h1 {
            color: $white;
        }
    }

    .up:hover .hover-corp {
        display: block;
    }

    img {
        width: 800px;
        height: 800px;
    }
}
</style>