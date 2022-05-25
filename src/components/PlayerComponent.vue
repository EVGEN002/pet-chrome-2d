<template>
  <div class="player-component" :style="playerPosition">
  </div>
</template>

<script>
export default {
  name: 'PlayerComponent',
  props: {
    xPlayerPosition: {
      type: Number,
      required: true
    },
    yPlayerPosition: {
      type: Number,
      required: true
    }
  },
  computed: {
    playerPosition () {
      return {
        bottom: this.yPlayerPosition + '%',
        left: this.xPlayerPosition + '%'
      }
    }
  }
}
</script>

<style lang="sass" scoped>
.player-component
  position: absolute

  background-color: blue

  height: 50px
  width: 40px
</style>
