<template>
    <div class="container-fluid">
        <div class="mycontainer">
            <div class="row">
                <div class="col">
                    <div class="bigger">
                        <img src="public\images\social-1.jpg" alt="social1">
                    </div>
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
                <div class="col">
                    <div class="bigger">
                        <img src="public\images\social-2.jpg" alt="social2">
                    </div>
                </div>
            </div>
            <div class="row pt-3">
                <div class="col-3" v-for="(social, index) in socials" :key="index">
                    <div class="bigger">
                        <img :src="social.img" :alt="social.title">
                    </div>
                </div>
            </div>

        </div>
    </div>
</template>

<script>
export default {
    name: 'SocialComp',
    data() {
        return {
            socials: [
                {
                    img: 'public/images/social-3.jpg',
                    title: 'social-3'
                },
                {
                    img: 'public/images/social-4.jpg',
                    title: 'social-4'
                },
                {
                    img: 'public/images/social-5.jpg',
                    title: 'social-5'
                },
                {
                    img: 'public/images/social-6.jpg',
                    title: 'social-6'
                }
            ]
        }
    },
}
</script>

<style lang="scss" scoped>
@use '../assets/partials/variables' as *;

img {
    width: 100%;
    transition: 2s;

}

.bigger {
    overflow: hidden;
}

.bigger:hover img {
    transform: scale(1.2);
    filter: opacity(0.9);

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