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
@media (max-width: 768px) {
  .contact__container {
    width: 90%;
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
