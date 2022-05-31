<template>
  <div class='game-screen-component vue-component'>
    <canvas class="canvas"></canvas>
  </div>
</template>

<script>
export default {
  name: 'game-screen-component',
  components: {},
  data: function () {
    return {}
  },
  props: [],
  computed: {},
  methods: {}
}
</script>

<style scoped='scoped' lang='sass'>
.game-screen-component
  height: 100%
  width: 100%

  canvas
    height: 100%
    width: 100%
</style>
