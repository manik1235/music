<template>
  <div class="xylophone-key">
    <div class="key" :style="styleObjectComputed">
      Key
    </div>
  </div>
</template>

<script>
export default {
  name: 'XylophoneKey',
  props: {
    styleObject: Object
  },
  computed: {
    styleObjectComputed() {
      var styleObject = { ...this.styleObject, ...{ height: this.styleObject.height + 'px' } }
      return styleObject
    }
  }
}
</script>

<style scoped>
.key {
  border-style: solid;
  border-width: 1px;
}
</style>
