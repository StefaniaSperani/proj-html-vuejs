<template>
    <div class="container-fluid">
        <div class="mycontainer">
            <div class="text-center">
                <p class="pre-title">Locations</p>
                <h2>Visit our Bakeries</h2>
            </div>

            <div class="d-flex flex-row py-5">
                <div class="newyork">
                    <div class="bigger">
                        <img src="/public/images/new-york-bk.jpg" alt="">
                    </div>
                    <div class="d-flex flex-column p-5">
                        <h2 class="text-center text-capitalize p-4">New York</h2>
                        <div class="d-flex flex-row justify-content-between pt-2">
                            <div class="pre-title d-flex flex-column text-center">Call us
                                <div class="fs-5">1.800.458.556</div>
                            </div>
                            <div class="pre-title d-flex flex-column text-center">Open all week
                                <span class="fs-5 text-uppercase">9:00.am - 6;00 pm</span>
                            </div>
                            <button class="mybutton">View map</button>
                        </div>
                    </div>
                </div>

                <div class="london">
                    <div class="bigger">
                        <img src="/public/images/london-bk.jpg" alt="">
                    </div>

                    <div class="d-flex flex-column p-5">
                        <h2 class="text-center text-capitalize p-4">London</h2>
                        <div class="d-flex flex-row justify-content-between pt-2">
                            <div class="pre-title d-flex flex-column text-center">Call us
                                <div class="fs-5">1.800.458.556</div>
                            </div>
                            <div class="pre-title d-flex flex-column text-center">Open all week
                                <span class="fs-5 text-uppercase">9:00.am - 6;00 pm</span>
                            </div>
                            <button class="mybutton">View map</button>
                        </div>
                    </div>
                </div>
            </div>
        </div>
    </div>
</template>

<script>
export default {
    name: 'StoresComp'
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/variables' as *;

img {
    width: 100%;
}

.newyork {
    background-color: $newyork;
    overflow: hidden;

}

.london {
    background-color: $london;
    overflow: hidden;
}

.bigger {
    transition: 2s;
}

.bigger:hover {
    transform: scale(1.2);
    filter: opacity(0.9);
}

.mybutton {
    color: $primary;
    background-color: $white;
    font-weight: bold;
    padding: 0.5em 1em;

    &:hover {
        background-color: $primary;
        color: $white;
    }
}
</style>