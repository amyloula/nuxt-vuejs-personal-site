<template>
  <form
    class="contact__form"
    name="contact"
    action="/thank-you"
    netlify-honeypot="bot-field"
    method="post"
    netlify
  >
    <div class="contact__form__left-panel">
      <img
        class="img"
        src="~/assets/imgs/stamp.svg"
        alt="Stamp icon"
        aria-label="Stamp icon"
      />
      <div class="text-wrapper">
        <p>Feel free to reach out to me about:</p>
        <ul>
          <li>Conferences</li>
          <li>Workshops</li>
          <li>Hackathons</li>
          <li>Mentorship</li>
        </ul>
        <p>
          Please try to be
          <span class="bold-text">as specific as possible in your request</span>
          so I can best help you.
        </p>
        <a
          href="https://twitter.com/intent/tweet?screen_name=amyloulala&ref_src=twsrc%5Etfw"
          class="twitter-mention-button"
          data-show-count="false"
          >Tweet to @amyloulala</a
        >
      </div>
    </div>
    <div class="contact__form__right-panel">
      <h2 class="header">Contact me</h2>
      <input type="hidden" name="form-name" value="contact" />
      <p hidden>
        <label>Don’t fill this out: <input name="bot-field"/></label>
      </p>
      <label class="form-label" for="name">Name:</label>
      <b-form-input
        id="name"
        name="name"
        placeholder="Enter your name"
      ></b-form-input>
      <label class="form-label" for="email">Email:</label>
      <b-form-input name="email" id="email" placeholder="Email"></b-form-input>
      <label class="form-label" for="message">Message:</label>
      <b-form-textarea
        id="message"
        name="message"
        placeholder="Enter something..."
        rows="3"
        max-rows="6"
      ></b-form-textarea>
      <div class="contact__form__btn-wrapper">
        <b-button variant="outline-dark" type="submit"
          >Send me a message</b-button
        >
      </div>
    </div>
  </form>
</template>

<script>
export default {
  head() {
    return {
      script: [
        {
          src: 'https://platform.twitter.com/widgets.js'
        }
      ]
    }
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/styles/_variables.scss';
.contact__form {
  background-color: $secondary-background-color;
  margin: 0 auto;
  display: flex;
  flex-direction: row;
  align-items: flex-end;
  padding: 1rem;
  font-family: $main-body-font;
  box-shadow: $main-box-shadow;
  &__left-panel {
    flex: 1;
    padding: 1rem;
    .img {
      height: 10rem;
      width: 10rem;
    }
    .text-wrapper {
      li:before {
        content: '🙆🏽‍♀️';
        margin-left: -20px;
        margin-right: 10px;
      }
    }
    .bold-text {
      font-family: $main-header-font;
    }
  }
  &__right-panel {
    flex: 1;
    padding: 1rem;
    align-self: center;
    .header {
      font-family: $main-header-font;
    }
  }
  &__btn-wrapper {
    flex: 1 1 100%;
    button {
      margin: 0.5rem 0;
      width: 100%;
    }
  }
}

@media only screen and (max-width: 1024px) {
  .contact__form {
    flex-direction: column;
    align-items: normal;

    &__left-panel {
      display: flex;
      flex-direction: column;

      img {
        align-self: end;
        height: 5rem;
        width: 5rem;
      }
    }

    &__right-panel {
      align-self: stretch;
    }
  }
}
</style>
