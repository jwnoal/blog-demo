<template>
  <div>
    <InputNumber :max="20" v-model="value7" />
    <InputNumber
      :max="20"
      v-model="value5"
      :formatter="(value) => `￥ ${value}`.replace(/\B(?=(\d{3})+(?!\d))/g, ',')"
      :parser="(value) => value.replace(/\￥\s?|(,*)/g, '')"
    />
    <br />
    <br />
    <br />
    <br />
  </div>
</template>
<script lang="ts">
import { Options, Vue } from 'vue-class-component'

@Options({})
export default class Myinput extends Vue {
  value1 = ''
  value2 = ''
  value3 = ''
  value4 = ''
  value5 = 1
  value6 = null
  value7 = null
  created(): void {}
}
</script>
<style lang="less" scoped></style>
