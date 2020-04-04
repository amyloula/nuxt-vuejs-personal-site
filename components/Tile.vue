<template>
  <div class="tile">
    <div class="tile__header">
      <b-icon-star v-if="tileInfo.stars === 0"></b-icon-star>
      <b-icon-star-fill v-if="tileInfo.stars > 0"></b-icon-star-fill>
      <b-badge variant="light">
        {{ tileInfo.stars }}
      </b-badge>
    </div>
    <div class="tile__content">
      <p>{{ tileInfo.name }}</p>
      <a :href="url" rel="noreferrer">
        <b-button variant="outline-light">View code</b-button>
      </a>
    </div>
  </div>
</template>
<script>
export default {
  props: ['tileInfo'],
  data() {
    return {
      url: this.tileInfo.url
    }
  }
}
</script>
<style lang="scss" scoped>
@import '~assets/styles/_variables.scss';
::-moz-selection {
  background: #faaca8;
}
::selection {
  background: #faaca8;
}
.tile {
  font-family: $main-body-font;
  text-align: center;
  height: 11rem;
  width: 9rem;
  margin: 1rem;
  padding: 0.5rem;
  border-radius: 5px;
  background: $gradient-background-color;
  background-image: $background-gradient;
  box-shadow: $main-box-shadow;
  display: flex;
  flex-direction: column;
  &__header {
    order: 0;
    flex: 1;
    align-self: end;
  }
  &__content {
    order: 1;
    flex: 1;
    color: white;
    word-wrap: break-word;
    p {
      font-family: $main-header-font;
    }
  }
}
</style>
