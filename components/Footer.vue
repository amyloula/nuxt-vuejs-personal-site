<template>
    <footer>
        <div class="footer container__wrapper">
            <div class="footer logo__wrapper">
                <img class="img" src="~/assets/imgs/nuxtjs.jpg" alt="Nuxtjs Logo" aria-label="Nuxtjs logo">
                <img class="img" src="~/assets/imgs/vuejs.svg" alt="Vue.js Logo" aria-label="Vue.js logo">
                <p>This site was built with Nuxt.js and Vue.js</p>
            </div>
        </div>
    </footer>
</template>

<script>
export default {

}
</script>

<style lang="scss" scoped>
@import "~assets/styles/_variables.scss";
.footer {
    .container__wrapper {
        width: 100%;
    }
    .logo__wrapper {
        margin: 0 auto;
        width: 50%;
        text-align: center;
        .img {
            height: 3rem;
            width: 3rem;
        }
    }
}
</style>