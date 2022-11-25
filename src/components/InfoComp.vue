<template>
    <div class="container-fluid">
        <div class="mycontainer row gap-4">
            <div class="col-12 px-0 position-relative">
                <img src="/public/images/bakery-process-1.jpg" alt="process">
                <div class="veil position-absolute">
                    <div class="d-flex justify-content-between align-items-center p-5">
                        <h1>Tell us what you have in mind</h1>
                        <p class="display-1 text-white">01</p>
                    </div>
                    <div class="d-flex justify-content-end align-items-end flex-column myposition-absolute1">
                        <div class="justify-self-start w-custom p-5">
                            <p class="pre-title">
                                Manual ingredients selection</p>
                            <p class="text-white">Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis
                                odio,
                                repellendus natus
                                neque illo quae error ipsum obcaecati omnis facere sed sunt, corrupti odit, adipisci
                                enim
                                quibusdam eaque ratione sint?</p>
                        </div>
                    </div>
                </div>
            </div>


            <div class="row">
                <div class="col-6 px-0 d-flex gap-4 position-relative">
                    <img src="/public/images/bakery-process-2.jpg" alt="process-2">
                    <div class="veil position-absolute">
                        <div class="d-flex justify-content-between align-items-center p-5">
                            <h1 class="text-capitalize">We start baking</h1>
                            <p class="display-1 text-white">02</p>
                        </div>
                        <div class="d-flex myposition-absolute">
                            <div class="justify-self-start w-custom p-5">
                                <p class="pre-title">
                                    Sweet and delicious</p>
                                <p class="text-white">Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis
                                    odio,
                                    repellendus natus
                                    neque illo quae error ipsum obcaecati omnis facere sed sunt, corrupti odit, adipisci
                                    enim
                                    quibusdam eaque ratione sint?</p>
                            </div>
                        </div>
                    </div>

                    <div class="col-6 cit">
                        <div class="pre-title">Dont just take our word for it</div>
                        <h1><i class="fa-solid fa-quote-left"></i>
                            Finally found an alternative to the mass produced products. Something that incorporates
                            real
                            organic ingredients, nutrient dense wellness while promoting sustainability and
                            activity.
                            <i class="fa-solid fa-quote-right"></i>
                        </h1>
                        <p class="pre-title">Rachel Cooper, Founder</p>
                    </div>
                </div>
            </div>


            <div class="col-12 px-0 position-relative">
                <img src="/public/images/bakery-process-3.jpg" alt="process-3">
                <div class="veil position-absolute">
                    <div class="d-flex justify-content-between align-items-center p-5">
                        <h1>Delivered to your home</h1>
                        <p class="display-1 text-white">03</p>
                    </div>
                    <div class="d-flex myposition-absolute">
                        <div class="justify-self-start w-custom p-5">
                            <p class="pre-title">
                                Baked to order & gift wrapped</p>
                            <p class="text-white">Lorem ipsum dolor sit amet consectetur adipisicing elit. Corporis
                                odio,
                                repellendus natus
                                neque illo quae error ipsum obcaecati omnis facere sed sunt, corrupti odit, adipisci
                                enim
                                quibusdam eaque ratione sint?</p>
                        </div>
                    </div>
                </div>
            </div>

        </div>

    </div>
</template>

<script>
export default {
    name: 'InfoComp',
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/variables' as *;

img {
    width: 100%;
    object-fit: cover;
}


.cit {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: flex-start;
    padding: 3em;
    background-color: $bg-section;
    width: 100%;

    h1 {
        padding: 1em 0;
    }

    p.pre-title {
        text-transform: capitalize;
    }
}

.veil {
    top: 0;
    bottom: 0;
    right: 0;
    left: 0;
    background-image: linear-gradient(to top left, rgba(0, 0, 0, 0.705), rgba(0, 0, 0, 0.082));

    h1 {
        color: $white;
    }

    p.pre-title {
        color: $text-opacity;
    }

    .w-custom {
        width: 600px;
    }

    .myposition-absolute {
        position: absolute;
        bottom: 0;
    }

    .myposition-absolute1 {
        position: absolute;
        bottom: 0;
        right: 0;
    }

}
</style>