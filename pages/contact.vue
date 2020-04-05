<template>
  <div class="contact__container">
    <ContactForm />
  </div>
</template>

<style lang="scss" scoped>
@import '~assets/styles/_variables.scss';

.contact__container {
  width: 50%;
  margin: 0 auto;
  font-family: $main-header-font;
  padding: 1rem;
}
@media only screen and (max-width: 768px) {
  .contact__container {
    width: 90%;
  }
}

/* Portrait and Landscape */
@media only screen and (min-width: 769px) and (max-width: 1024px) and (-webkit-min-device-pixel-ratio: 2) {
  .contact__container {
    width: 75%;
  }
}
</style>

<script>
import ContactForm from '~/components/ContactForm.vue'

export default {
  components: {
    ContactForm
  }
}
</script>
