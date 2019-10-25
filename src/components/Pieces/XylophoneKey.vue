<template>
  <div class="xylophone-key">
    <div class="key" :style="styleObject">
      Key
    </div>
  </div>
</template>

<script>
export default {
  name: 'XylophoneKey',
  props: {
    styleObject: String
  }
}
</script>

<style scoped>
</style>
