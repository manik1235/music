<template>
  <div class="XylophoneAlpha">
    <div class="keyboard" :style="{ height: maxHeight + 'px' }">
      <table>
        <tr>
          <td v-for="kee in kees" :key="kee.id">
            <div :style="{ height: kee.height + 'px' }">
              <XylophoneKey :styleObject="kee"/>
            </div>
          </td>
        </tr>
      </table>
    </div>
  </div>
</template>

<script>
import XylophoneKey from '../Pieces/XylophoneKey.vue'

export default {
  data() {
    return {
      baseKeyHeight: 200,
      keyboardPadding: 2.7
    }
  },
  computed: {
    maxHeight() {
      return Math.max(...this.kees.map(kee => kee.height)) * this.keyboardPadding
    },
    kees() {
      return [
        { borderColor: 'red', color: 'red', height: this.baseKeyHeight },
        { borderColor: 'orange', color: 'orange', height: this.baseKeyHeight * 5/6 },
        { borderColor: 'yellow', color: 'yellow', height: this.baseKeyHeight * 4/6 },
        { borderColor: 'green', color: 'green', height: this.baseKeyHeight * 3/6 },
        { borderColor: 'blue', color: 'blue', height: this.baseKeyHeight * 2/6 },
        { borderColor: 'purple', color: 'purple', height: this.baseKeyHeight * 1/6 }
      ]
    }
  },
  components: {
    XylophoneKey
  }
}
</script>

<style scoped>
.keyboard {
  border-color: blue;
  border-style: solid;
  border-width: 1px;
}
</style>
