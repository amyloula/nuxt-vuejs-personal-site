<template>
  <div class="card">
    <div class="card-content">
      <h3 class="headline">{{ headline }}</h3>
      <p v-for="(item, index) in text" v-bind:key="index">{{ item }}</p>
      <hr />
    </div>
  </div>
</template>

<script>
export default {
  name: 'Card',
  props: {
    headline: String,
    text: Array
  }
}
</script>

<style lang="scss" scoped>
@import '~assets/styles/_variables.scss';

hr {
  border: 1px dashed $gradient-background-color;
}
.card {
  background-color: white;
  border-radius: 5px;
  box-shadow: 0 20px 60px 0 #e0c3fc;
  width: 28rem;
  height: 28rem;
  padding: 10px;
}

.headline {
  font-weight: bold;
}

.card-icon {
  pointer-events: none;
  width: 180px;
  padding: 40px 20px 0px 20px;
}

.card-content {
  padding: 20px;
}

@media (max-width: 768px) {
  .card {
    width: 90%;
    margin: 0 auto;
  }
}
</style>
