<template>
    <div class="container-fluid">
        <div class="mycontainer">
            <div class="row">
                <div class="col hover">
                    <img src="public\images\social-1.jpg" alt="">
                </div>
                <div class="col-6">
                    <div class="socials">
                        <p class="pre-title">
                            Made for sharing
                        </p>
                        <h2>Lets stay in touch</h2>
                        <button class="mybutton text-capitalize"> <i class="fa-brands fa-instagram"></i> Follow
                            us</button>
                    </div>
                </div>
                <div class="col hover">
                    <img src="public\images\social-2.jpg" alt="">
                </div>
            </div>
            <div class="row pt-3">
                <div class="col-3 hover">
                    <img src="public\images\social-3.jpg" alt="">
                </div>
                <div class="col-3 hover">
                    <img src="public\images\social-4.jpg" alt="">
                </div>
                <div class="col-3 hover">
                    <img src="public\images\social-5.jpg" alt="">
                </div>
                <div class="col-3 hover">
                    <img src="public\images\social-6.jpg" alt="">
                </div>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'SocialComp'
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/variables' as *;

img {
    width: 100%;
}


.hover:hover img {
    overflow: hidden;
    opacity: 0.8;
}

.socials {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    padding: 3em;
    background-color: $bg-section;
    width: 100%;
    height: 100%;
}
</style>