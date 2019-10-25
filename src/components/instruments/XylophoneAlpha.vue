<template>
  <div class="XylophoneAlpha">
    <table>
      <tr :style="{ height: this.maxHeight }">
        <td v-for="kee in kees" :key="kee.id">
          <div :style="{ height: kee.height + 'px' }">
            <XylophoneKey :styleObject="kee"/>
          </div>
        </td>
      </tr>
    </table>
  </div>
</template>

<script>
import XylophoneKey from '../Pieces/XylophoneKey.vue'

export default {
  data() {
    return {
      kees: [
        { color: 'red', height: 10 },
        { color: 'orange', height: 10 },
        { color: 'yellow', height: 10 },
        { color: 'green', height: 10 },
        { color: 'blue', height: 10 },
        { color: 'purple', height: 10 },
      ]
    }
  },
  computed: {
    maxHeight: {}
  },
  components: {
    XylophoneKey
  }
}
</script>

<style scoped>
</style>
