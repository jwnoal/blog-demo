<template>
  <input @input="change" @change="change" :value="currentValue" placeholder="请输入数字" />
</template>
<script lang="ts">
import { Options, Vue } from 'vue-class-component'

class Props {
  max?: number
}

@Options({
  components: {}
})
export default class NumberInput extends Vue.with(Props) {
  currentValue = null
  created(): void {}
  mounted(): void {}
  change(event) {
    let val = event.target.value.trim()
    if (event.type === 'input' && val.match(/^\-?\.?$|\.$/)) return // prevent fire early if decimal. If no more input the change event will fire later
    val = Number(val)

    console.log('--', val)

    if (!isNaN(val)) {
      this.currentValue = val
    } else {
      this.currentValue = event.target.value = null
    }
    console.log(this.currentValue, event.target.value)
  }
}
</script>
<style lang="less" scoped></style>
