<template>
  <div class="screen-component">
    <PlayerComponent :xPlayerPosition="xPlayerPosition" :yPlayerPosition="yPlayerPosition"
    @pressRight="pressRight()"
    @pressLeft="pressLeft()"
    @pressUp="pressUp()"
    @pressDown="pressDown()"
    />
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
  data () {
    return {
      xPlayerPosition: 10,
      yPlayerPosition: 20,
      requestFrame: undefined
    }
  },
  methods: {
    mainCycle () {
      this.request = requestAnimationFrame(this.mainCycle)
    }
  },
  mounted () {
    this.mainCycle()
  }
}
</script>

<style lang="sass" scoped>
.screen-component
  width: 100vw
  height: 100vh
  background-color: #000000
</style>
