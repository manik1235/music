<template>
  <div class="XylophoneAlpha">
    <table>
      <tr>
        <td v-for="kee in kees" :key="kee.id">
          <XylophoneKey :styleObject="kee"/>
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
        { color: 'red' },
        { color: 'orange' }
      ]
    }
  },
  components: {
    XylophoneKey
  }
}
</script>

<style scoped>
</style>
