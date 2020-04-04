<template>
  <div class="about-me">
    <div class="about-me header__container">
      <h3>About me</h3>
    </div>
    <section class="about-me main__container">
      <div class="main__container--left">
        <img
          src="~/assets/imgs/me.JPG"
          alt="Amy Louise McCabe"
          aria-label="Picture of Amy Louise McCabe"
        />
      </div>
      <div class="about-me main__container--right">
        <div class="about-me text__wrapper">
          <h1>I'm serious as a heart attack</h1>
          <p>
            The path of the righteous man is beset on all sides by the
            iniquities of the selfish and the tyranny of evil men. Blessed is he
            who, in the name of charity and good will, shepherds the weak
            through the valley of darkness, for he is truly his brother's keeper
            and the finder of lost children. And I will strike down upon thee
            with great vengeance and furious anger those who would attempt to
            poison and destroy My brothers. And you will know My name is the
            Lord when I lay My vengeance upon thee.
          </p>

          <!-- end slipsum code -->
        </div>
        <SocialIcon
          v-for="icon in socialProfiles"
          :key="icon.label"
          :socialInfo="icon"
        />
      </div>
    </section>
  </div>
</template>
<style lang="scss" scoped>
@import '~assets/styles/_variables.scss';
.content-wrapper {
  background-color: $gradient-background-color;
  background-image: $background-gradient;
}
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

  .text__wrapper {
    padding: 5rem;
  }

  .main__container {
    text-align: center;
    font-family: $main-header-font;
    display: flex;
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
    img {
      height: 25rem;
      width: 25rem;
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

      > img {
        flex: 1;
        justify-content: center;
      }
    }
    &--left {
      flex: 1;
      order: 0;
      align-self: center;
    }
    &--right {
      background-color: white;
      order: 1;
      flex: 1;
    }
  }
}
</style>
<script>
import SkillsComponent from '~/components/Skills.vue'
import SocialIcon from '~/components/SocialIcon.vue'
export default {
  components: {
    SkillsComponent,
    SocialIcon
  },
  data() {
    return {
      socialProfiles: [
        {
          link: 'https://github.com/amyloula',
          img: 'github-light.svg',
          label: 'Github'
        },
        {
          link: 'https://stackoverflow.com/users/4203782/amyloula',
          img: 'stackoverflow.svg',
          label: 'Stackoverflow'
        },
        {
          link: 'https://twitter.com/amyloulala',
          img: 'twitter.svg',
          label: 'Twitter'
        },
        {
          link: 'https://www.linkedin.com/in/amylouisemccabe/',
          img: 'linkedin.svg',
          label: 'Linkedin'
        }
      ]
    }
  },
  methods: {}
}
</script>
