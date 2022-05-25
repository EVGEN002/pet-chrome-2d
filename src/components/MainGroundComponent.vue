<template>
  <div class="main-ground-component" :style="{ 'height': height + '%' }">
  {{ height }}
  </div>
</template>

<script>
export default {
  name: 'MainGroundComponent',
  props: {
    height: {
      type: Number,
      required: true
    }
  }
}
</script>

<style lang="sass" scoped>
.main-ground-component
  position: absolute
  bottom: 0
  left: 0

  width: 100%
  background-color: #ffffff
</style>
