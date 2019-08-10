<template>
    <div class="main__body">
        <img src="~/assets/imgs/me.JPG" alt="Amy Louise McCabe" aria-label="Picture of Amy Louise McCabe">
        <section class="main__body__top">
            <h1>Hi, I'm Amy.</h1>
            <h2>I'm a Software developer specialist, working at the Dock - Accenture’s global centre for innovation in Dublin.
            </h2>
            <p>
                I'm part of the CIO, a global team that provides best in class technology and employee experiences to support Accenture’s high-performance workforce. CIO brings cutting edge technologies and approaches together to deliver at scale across a global enterprise.
            </p>
        </section>
        <section class="main__body--bottom">
            <p>Where you can find me online:</p>
            <a href="https://github.com/amyloula" target="_blank" rel="noreferrer">
                    <img class="img" src="~/assets/imgs/github-light.svg" alt="Github" aria-label="Github icon">
                </a>
            <a href="https://stackoverflow.com/users/4203782/amyloula" target="_blank" rel="noreferrer">
                    <img class="img" src="~/assets/imgs/stackoverflow.svg" alt="Stackoverflow"
                        aria-label="Stack Overflow icon">
                </a>
            <a href="https://twitter.com/amyloulala" target="_blank" rel="noreferrer">
                    <img class="img" src="~/assets/imgs/twitter.svg" alt="Twitter" aria-label="Twitter icon">
                </a>
            <a href="https://www.linkedin.com/in/amylouisemccabe/" target="_blank" rel="noreferrer">
                    <img class="img" src="~/assets/imgs/linkedin.svg" alt="Twitter" aria-label="Linkedin icon">
                </a>
        </section>
        <section class="main__body--skills">
            <p>Tools that I work with:</p>
            <div class="skills__wrapper">
                <img class="img" src="~/assets/imgs/js.svg" alt="Javascript Logo" aria-label="Javascript logo">
                <img class="img" src="~/assets/imgs/node.svg" alt="Node Logo" aria-label="Node logo">
                <img class="img" src="~/assets/imgs/angular.svg" alt="Angular Logo" aria-label="Angular logo">
                <img class="img" src="~/assets/imgs/react.svg" alt="React Logo" aria-label="React logo">
                <img class="img" src="~/assets/imgs/typescript.svg" alt="Typescript Logo" aria-label="Typescript logo">
                <img class="img" src="~/assets/imgs/cloud-functions.svg" alt="GCP Cloud functions Logo" aria-label="GCP Cloud functions logo">
                <img class="img" src="~/assets/imgs/ionic.svg" alt="Ionic Logo" aria-label="Ionic logo">
                <img class="img" src="~/assets/imgs/sass.svg" alt="Sass Logo" aria-label="Sass logo">
                <img class="img" src="~/assets/imgs/npm.svg" alt="Npm Logo" aria-label="Npm logo">
            </div>
    
        </section>
    </div>
</template>

<style lang="scss" scoped>
@import "~assets/styles/_variables.scss";
body {
    background: $main-background-color;
    color: $main-body-color;
}

.main__body {
    text-align: center;
    width: 75%;
    margin: $center-margin;
    img {
        height: 150px;
        width: 150px;
        border-radius: 50%;
        &:hover {
            filter: grayscale(100%);
            transition: all 0.5s ease;
        }
    }
    &__top {
        h1 {
            font-family: $main-header-font;
            font-weight: 700;
        }
        h2 {
            font-family: $main-header-font;
        }
        p {
            font-family: $main-body-font;
        }
    }
    &--bottom,
    &--skills {
        font-family: $main-body-font;
        p {
            font-family: $main-header-font;
        }
        a {
            text-decoration: none;
        }
        .img {
            height: 50px;
            width: 50px;
            border-radius: 0;
            &:hover {
                filter: opacity(50%);
            }
        }
    }
    &--skills {
        .skills__wrapper {
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