<template>
  <div class="app main">
    <GameScreenComponent />
  </div>
</template>

<script>
import GameScreenComponent from './components/GameScreenComponent.vue'

export default {
  name: 'App',
  components: {
    GameScreenComponent
  }
}
</script>

<style lang="sass">
@import "./assets/main.sass"
.app
  height: 100%
  width: 100%
</style>
