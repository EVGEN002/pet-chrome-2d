<template>
  <div class="app main">
    <ScreenComponentVue />
  </div>
</template>

<script>
import ScreenComponentVue from './components/ScreenComponent.vue'

export default {
  name: 'App',
  components: {
    ScreenComponentVue
  }
}
</script>

<style lang="sass">
@import "./assets/main.sass"
</style>
