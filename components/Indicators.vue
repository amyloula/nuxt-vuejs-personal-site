<template>
  <ul>
    <li
      v-for="(_, index) in elements"
      class="dot"
      :key="index"
      @click="showElement(index)"
      :class="{ 'dot-selected': currentElementIndex === index }"
    >
      <button class="indicator-btn" :disabled="currentElementIndex === index" />
    </li>
  </ul>
</template>

<script>
export default {
  name: 'Indicators',
  props: { elements: Array, currentElementIndex: Number, showElement: Function }
}
</script>
<style lang="scss" scoped>
@import '~assets/styles/_variables.scss';
@import '~assets/styles/animations.scss';

ul {
  list-style-type: none;
  padding: 0;
}

li {
  display: inline-block;
  margin: 0 10px;
}
.dot {
  height: 1rem;
  width: 1rem;
  border-radius: 50%;
  border: 3px solid $gradient-background-color;
  opacity: 0.2;
  cursor: pointer;
  position: relative;
}

.dot-selected {
  background-color: $gradient-background-color;
  opacity: 0.7;
  cursor: default;
  animation: fadeIn ease 2s;
  -webkit-animation: fadeIn ease 2s;
  -moz-animation: fadeIn ease 2s;
  -o-animation: fadeIn ease 2s;
  -ms-animation: fadeIn ease 10s;
  animation-fill-mode: forwards;
}

.indicator-btn {
  position: absolute;
  left: 0px;
  padding: 0px;
  height: 10px;
  width: 10px;
  border-radius: 50%;
  background: transparent;
  border: none;
}
</style>
