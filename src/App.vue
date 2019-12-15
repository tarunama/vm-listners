<template>
  <div class="app">
    <p>{{ clickCountText }}</p>  
    <p>{{ clickMouseOverText }}</p>  
    <child-component
      @click="incrementClickCount()"
      @mouseover="incrementMouseOverCount()"
    ></child-component>
  </div>
</template>

<script>
import ChildComponent from './components/ChildComponent.vue'

export default {
  name: 'app',
  components: {
    ChildComponent
  },
  computed: {
    clickCountText() {
      return `clickCount: ${this.clickCount}`
    },
    clickMouseOverText() {
      return `mouseOverCount: ${this.mouseOverCount}`
    }
  },
  data() {
    return {
      clickCount: 0,
      mouseOverCount: 0
    }
  },
  methods: {
    incrementClickCount() {
      this.clickCount++
    },
    incrementMouseOverCount() {
      this.mouseOverCount++
    }
  }
}
</script>

<style>
.app {
  text-align: center;
}
</style>
