<template>
  <div class="player-component" tabindex="0" v-focus :style="playerPosition"
  @keydown.right="$emit('pressRight')"
  @keydown.left="$emit('pressLeft')"
  @keydown.up="$emit('pressUp')"
  @keydown.down="$emit('pressDown')"
  >
  </div>
</template>

<script>
import PlayerInterface from '../mixins/PlayerInterface'

export default {
  name: 'PlayerComponent',
  mixins: [PlayerInterface],
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
