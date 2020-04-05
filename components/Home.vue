<template>
  <div class="main__body">
    <div class="main__body__left">
      <img
        src="~/assets/imgs/me.JPG"
        alt="Amy Louise McCabe"
        aria-label="Picture of Amy Louise McCabe"
      />
    </div>
    <section class="main__body__right">
      <h1>Hi, I'm Amy.</h1>
      <h5>
        I'm a Software developer specialist, working at the Dock - Accenture’s
        global centre for innovation in Dublin.
      </h5>
      <n-link to="/about-me" no-prefetch>
        <b-button variant="outline-dark">Find out more about me</b-button>
      </n-link>
    </section>
  </div>
</template>
<style lang="scss" scoped>
@import '~assets/styles/_variables.scss';
.main__body {
  display: flex;
  flex-direction: row;
  align-items: center;
  justify-content: center;
  margin-top: 3rem;
  &__left {
    img {
      height: 25rem;
      width: 25rem;
      vertical-align: baseline;
      transition: 0.3s;
      &:hover {
        box-shadow: 0 8px 6px -6px #e0c3fc;
      }
    }
  }
  &__right {
    background-color: white;
    box-shadow: $main-box-shadow;
    margin-left: -3rem;
    width: 30%;
    padding: 3rem;
    transition: 0.3s;
    border: 1px solid black;

    &:hover {
      box-shadow: 0 8px 6px -6px $gradient-background-color;
    }
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
  }

  @media only screen and (max-width: 768px) {
    .main__body {
      flex-direction: column;
    }
  }

  // @media only screen and(min-width: 769px) and (max-width: 1024px) {
  //   .main__body {
  //     flex-direction: column;
  //   }
  // }
}
</style>
