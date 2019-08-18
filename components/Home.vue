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
      <h5>I'm a Software developer specialist, working at the Dock - Accenture’s global centre for innovation in Dublin.</h5>
      <!-- <p>I'm part of the CIO, a global team that provides best in class technology and employee experiences to support Accenture’s high-performance workforce. CIO brings cutting edge technologies and approaches together to deliver at scale across a global enterprise.</p> -->
      <n-link to="/about-me" no-prefetch>
        <b-button variant="outline-dark">Find out more about me</b-button>
      </n-link>
    </section>
  </div>
</template>

<style lang="scss" scoped>
@import '~assets/styles/_variables.scss';
body {
  background: $main-background-color;
  color: $main-body-color;
}

.main__body {
  text-align: center;
  width: 75%;
  margin: $center-margin;
  &__left {
    display: inline-block;
    img {
      height: 25rem;
      width: 25rem;
      vertical-align: baseline;
    }
  }
  &__right {
    background-color: white;
    box-shadow: $main-box-shadow;
    margin-left: -3rem;
    display: inline-block;
    width: 50%;
    padding: 3rem;
    transition: all 0.6s cubic-bezier(0.165, 0.84, 0.44, 1);

    &:hover {
      box-shadow: 0 8px 6px -6px teal;
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

  @media (max-width: 768px) {
    .main__body {
      width: 90%;
    }
    &__right {
      display: block;
      width: auto;
      margin-left: 0;
    }
    &__left {
        img {
            width: 100%;
        }
    }
  }
}
</style>