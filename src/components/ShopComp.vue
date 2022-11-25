<template>
    <div class="container-fluid bg-img">
        <div class="container p-custom">
            <p class="pre-title">Try our seasonal products</p>
            <h1 class="text-white w-50">Order for pick-up or delivery to your home</h1>
            <button class="mybutton mt-5">Shop now</button>
        </div>

    </div>
</template>

<script>
export default {
    name: 'ShopComp'
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/variables' as *;

.bg-img {
    background-image: url(/public/images/call-to-action-bg.jpg);
    background-size: cover;
    background-repeat: no-repeat;
    max-width: 100%;
    height: auto;

    .p-custom {
        padding: 8em 0;
    }

    p.pre-title {
        color: $text-opacity;
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