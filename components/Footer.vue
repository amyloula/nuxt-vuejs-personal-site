<template>
    <footer class="footer">
        <div class="footer logo__wrapper">
            <p>This site was built with Nuxt.js and Vue.js</p>
            <p>Hosted on Netlify</p>
            <img class="img" src="~/assets/imgs/nuxtjs.jpg" alt="Nuxtjs Logo" aria-label="Nuxtjs logo">
            <img class="img" src="~/assets/imgs/vuejs.svg" alt="Vue.js Logo" aria-label="Vue.js logo">
            <img class="img" src="~/assets/imgs/netlify.svg" alt="Netlify Logo" aria-label="Netlify logo">
            <p>
            © Amy McCabe 2019
            </p>
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
    height: auto;
    width: 100%;
    padding: 2rem;
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