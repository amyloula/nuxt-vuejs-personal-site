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
        <Carousel :cards="cards" />
        <SocialIcon
          v-for="icon in socialProfiles"
          :key="icon.label"
          :socialInfo="icon"
        />
      </div>
    </section>
  </div>
</template>
<script>
import SkillsComponent from '~/components/Skills.vue'
import Carousel from '~/components/Carousel.vue'
import SocialIcon from '~/components/SocialIcon.vue'
export default {
  components: {
    SkillsComponent,
    SocialIcon,
    Carousel
  },
  data() {
    return {
      cards: [
        {
          headline: 'Software Engineer',
          text: [
            'Specialist in JavaScript, TypeScript, Node.js, Angular.',
            'Experienced in React, Redux, rxjs, Vue.js, Nuxt.js, Python, Django, Ruby, PHP.'
          ]
        },
        {
          headline: 'Women in tech advocate',
          text: [
            'WWCode Network Evangelist',
            'GDG Cloud Organizer',
            'Women Techmakers Ambassador.'
          ]
        },
        {
          headline: 'Human being',
          text: [
            'Wife 👰🏽, animal lover 🐶, bookworm 📚, yogi 🧘🏽‍♀️, skin care enthusiast 🧴, emoji fluent 🤓, avid gif sharer 🤲🏽, electronic music lover ⚡️',
            'Polygot - english 🏴󠁧󠁢󠁥󠁮󠁧󠁿, spanish 🇪🇸, catalan 🎗, portuguese 🇧🇷, arabic 🇴🇲 '
          ]
        }
      ],
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
<style lang="scss" scoped>
@import '~assets/styles/_variables.scss';
.content-wrapper {
  background-color: $gradient-background-color;
  background-image: $background-gradient;
}
.about-me {
  margin: $center-margin;
  position: relative;
  .header__container {
    text-align: center;
    padding-bottom: 3rem;
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
      align-self: stretch;
    }
    &--right {
      background-color: white;
      order: 1;
      flex: 1;
    }
  }
}

@media (max-width: 768px) {
  .about-me {
    .main__container {
      flex-direction: column;

      img {
        width: 90%;
        height: auto;
      }

      &--right {
        margin-top: 2rem;
      }
    }
  }
}

@media only screen and (max-width: 1024px) {
}
</style>
