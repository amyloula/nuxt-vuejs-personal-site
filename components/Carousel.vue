<template>
  <div class="card-carousel__wrapper">
    <div class="card-carousel">
      <ArrowButton
        arrowType="left"
        @click.native="showPrevElement"
        :disabled="this.reachedMaxLeft"
      />
      <Card
        class="current-element"
        ref="card"
        :headline="currentElement.headline"
        :text="currentElement.text"
      />
      <ArrowButton
        arrowType="right"
        @click.native="showNextElement"
        :disabled="this.reachedMaxRight"
      />
    </div>
    <Indicators
      :elements="this.cards"
      :currentElementIndex="this.currentElementIndex"
      :showElement="this.showElement"
    />
  </div>
</template>
<script>
import Card from './Card.vue'
import ArrowButton from './ArrowButton.vue'
import Indicators from './Indicators.vue'

export default {
  name: 'Carousel',
  props: { cards: Array },
  components: { Card, ArrowButton, Indicators },

  data() {
    return {
      currentElementIndex: 0
    }
  },
  computed: {
    currentElement() {
      return this.cards[this.currentElementIndex]
    },
    reachedMaxLeft() {
      return this.currentElementIndex === 0
    },
    reachedMaxRight() {
      return this.currentElementIndex === this.cards.length - 1
    }
  },
  methods: {
    showNextElement() {
      this.currentElementIndex++
    },
    showPrevElement() {
      this.currentElementIndex--
    },
    showElement(elementIndex) {
      this.currentElementIndex = elementIndex
    }
  }
}
</script>
<style lang="scss" scoped>
@import '~assets/styles/animations.scss';
.fade-in {
  animation: fadeIn ease 2s;
  -webkit-animation: fadeIn ease 10s;
  -moz-animation: fadeIn ease 2s;
  -o-animation: fadeIn ease 10s;
  -ms-animation: fadeIn ease 10s;
  animation-fill-mode: forwards;
}
.card-carousel {
  display: flex;
  align-items: center;
  margin-bottom: 30px;
  &__wrapper {
    display: flex;
    align-items: center;
    flex-direction: column;
  }
}
.btn {
  height: 90px;
  border: none;
  background: transparent;
  cursor: pointer;
  opacity: 0.5;
}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (max-width: 768px) {
  .btn {
    display: none;
  }
}

.btn:focus {
  outline: none;
}

.btn:hover {
  opacity: 0.7;
}

.btn:disabled {
  opacity: 0.2;
  cursor: default;
}

.icon {
  height: 90px;
  width: auto;
}
</style>
