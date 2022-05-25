<template>
  <div class="screen-component">
    <PlayerComponent  :xPlayerPosition="xPlayerPosition" :yPlayerPosition="yPlayerPosition" v-on:keydown="pressRightRow()" />
    <MainGroundComponentVue :height="20" />
  </div>
</template>

<script>
import MainGroundComponentVue from './MainGroundComponent.vue'
import PlayerComponent from './PlayerComponent.vue'

export default {
  name: 'ScreenComponent',
  components: {
    MainGroundComponentVue,
    PlayerComponent
  },
  props: {
    xPlayerPosition: {
      type: Number,
      required: true
    },
    yPlayerPosition: {
      type: Number,
      required: true
    }
  }
}
</script>

<style lang="sass" scoped>
.screen-component
  width: 100vw
  height: 100vh
  background-color: #000000
</style>
