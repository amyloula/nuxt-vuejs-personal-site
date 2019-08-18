<template>
    <div class="about-me">
        <div class="about-me header__container">
            <h3>About me</h3>
        </div>
        <section class="about-me main__container">
            <p>Where you can find me online:</p>
            <a href="https://github.com/amyloula" target="_blank" rel="noreferrer">
            <img class="img" src="~/assets/imgs/github-light.svg" alt="Github" aria-label="Github icon">
            </a>
            <a href="https://stackoverflow.com/users/4203782/amyloula" target="_blank" rel="noreferrer">
            <img class="img" src="~/assets/imgs/stackoverflow.svg" alt="Stackoverflow" aria-label="Stack Overflow icon">
            </a>
            <a href="https://twitter.com/amyloulala" target="_blank" rel="noreferrer">
            <img class="img" src="~/assets/imgs/twitter.svg" alt="Twitter" aria-label="Twitter icon">
            </a>
            <a href="https://www.linkedin.com/in/amylouisemccabe/" target="_blank" rel="noreferrer">
            <img class="img" src="~/assets/imgs/linkedin.svg" alt="Twitter" aria-label="Linkedin icon">
            </a>
        </section>
        <section class="about-me secondary__container">
            <p>Languages I work with</p>
            <div class="content__wrapper">
                <img class="img" src="~/assets/imgs/js.svg" alt="Javascript Logo" aria-label="Javascript logo">
                <img class="img" src="~/assets/imgs/node.svg" alt="Node Logo" aria-label="Node logo">
                <img class="img" src="~/assets/imgs/typescript.svg" alt="Typescript Logo" aria-label="Typescript logo">
                <img class="img" src="~/assets/imgs/python.svg" alt="Python Logo" aria-label="Python logo">
            </div>
            <p>Frameworks I work with</p>
            <div class="content__wrapper">
                <img class="img" src="~/assets/imgs/angular.svg" alt="Angular Logo" aria-label="Angular logo">
                <img class="img" src="~/assets/imgs/react.svg" alt="React Logo" aria-label="React logo">
                <img class="img" src="~/assets/imgs/ionic.svg" alt="Ionic Logo" aria-label="Ionic logo">
                <img class="img" src="~/assets/imgs/django.svg" alt="Django Logo" aria-label="Django logo">
            </div>
            <p>Tools I work with</p>
            <div class="content__wrapper">
                <img class="img" src="~/assets/imgs/sass.svg" alt="Sass Logo" aria-label="Sass logo">
                <img class="img" src="~/assets/imgs/npm.svg" alt="Npm Logo" aria-label="Npm logo">
                <img class="img" src="~/assets/imgs/yarn.svg" alt="Yarn Logo" aria-label="Yarn logo">
            </div>
            <p>Cloud providers I work with</p>
            <div class="content__wrapper">
                <img class="img" src="~/assets/imgs/gcp.svg" alt="GCP Logo" aria-label="GCP logo">
                <img class="img" src="~/assets/imgs/aws.svg" alt="AWS Logo" aria-label="AWS logo">
                <img class="img" src="~/assets/imgs/netlify-full.svg" alt="Netlify Logo" aria-label="Netlify logo">
                <img class="img" src="~/assets/imgs/azure.svg" alt="Azure Logo" aria-label="Azure logo">
            </div>
            
        </section>
    </div>
</template>
<style lang="scss" scoped>
@import "~assets/styles/_variables.scss";
.about-me {
    padding-top: 1rem;
    margin: $center-margin;
    position: relative;
    .header__container {
        text-align: center;
        h3 {
            font-family: $main-header-font;
        }
    }
    .main__container,
    .secondary__container {
        text-align: center;
        font-family: $main-header-font;
        h1 {
            font-family: $main-header-font;
            font-weight: 700;
        }
        h5 {
            font-family: $main-header-font;
        }
        p {
            font-family: $main-body-font;
        }
        a {
            text-decoration: none;
        }
    }
    .main__container,
    .secondary__container {
        p {
            font-family: $main-header-font;
        }
        .img {
            height: 50px;
            width: 50px;
            border-radius: 0;
            &:hover {
                filter: opacity(50%);
            }
        }
        .content__wrapper {
            display: flex;
            flex-wrap: wrap;
            width: 50%;
            margin: $center-margin;
            >img {
                flex: 1;
                justify-content: center;
            }
        }
    }
}
</style>