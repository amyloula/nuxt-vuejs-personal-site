<template>
  <div class="skill">
    {{skillInfo.title}}
    <progress
      ref="skill"
      :after-load-value="skillInfo.value"
      value="0"
      max="100"
      style="background-color:orange;"
    ></progress>
  </div>
</template>

<script>
export default {
  props: ['skillInfo'],
  beforeMount: function() {},
  mounted: function() {
    this.$refs.skill.style.transitionDelay = '0.5s'
    this.$refs.skill.value = this.$refs.skill.attributes[0].nodeValue
  }
}
</script>

<style scoped lang="scss">
progress[value]::-webkit-progress-value {
  transition-delay: 1s;
  transition: width 0.5s;
  background: orange;
}
progress {
  width: 400px;
  border: 0;
  background-color: white;
  border: 1px solid black;
  overflow: hidden;
}
::-webkit-progress-value {
  transition: width 1s;
}
::-webkit-progress-bar {
  background-color: white;
}
</style>