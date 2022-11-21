<template>
    <div class="container-fluid">
        <div class="mycontainer text-center">
            <p class="pre-title">
                Corporate & weddings
            </p>
            <h1>Baking special moments</h1>
            <div class="moments">
                <img class="up" src="public\images\corporate-bg.jpg" alt="Corporate">
                <!-- <div class="hover-corp">
                    <img class="down" src="public\images\corporate-hover-bg.jpg" alt="CorporateHover">
                    <div class="hover-text">
                        <p class="pre-title">
                            International bakery
                        </p>
                        <h1>Corporate events</h1>
                        <button class="mybutton">Explore more</button>
                    </div>
                </div> -->
                <img src="public\images\wedding-bg.jpg" alt="Wedding">
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

    .hover-corp {
        display: none;
        position: relative;
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


    &:hover down {
        display: inline-block;
    }

    img {
        width: 800px;
        height: 800px;
    }
}
</style>