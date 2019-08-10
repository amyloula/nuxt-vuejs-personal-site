<template>
    <div class="contact__container">
        <ContactForm/>
    </div>
</template>

<style lang="scss" scoped>
@import "~assets/styles/_variables.scss";
.contact__container {
    font-family: $main-header-font;
    width: 90%;
    margin: 0 auto;
    padding: 1rem;
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