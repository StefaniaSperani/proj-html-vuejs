<template>
    <div class="container-fluid jumbo">
        <div class="mycontainer col-lg-5 col-md-8 col-sm-12">
            <div class="jumbo-txt">
                <p class="pre-title">Fresh & tasty bakery every day</p>
                <h1>The perfect fresh bread</h1>
                <p>Lorem ipsum dolor sit amet consectetur adipisicing elit. Necessitatibus quos officiis
                    quia! Odio ea, id quaerat ipsum minima quisquam aperiam aliquid laudantium aut accusamus nihil,
                    nesciunt
                    fuga. Nam, possimus nisi.</p>
                <button class="mybutton">Explore our products</button>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'JumboComp'
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/variables' as *;

.jumbo {
    background-image: url(/public/images/hero-header-bakery.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    background-position: 0 -30px;
    max-width: 100%;
    height: auto;

    .jumbo-txt {
        padding: 12em 0;
    }

    h1 {
        text-transform: capitalize;
    }

    .mybutton {
        color: $primary;
        background-color: $white;
        font-weight: bold;

        &:hover {
            background-color: $primary;
            color: $white;
        }
    }
}
</style>