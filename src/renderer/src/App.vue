<template>
  <myinput-demo></myinput-demo>
  <br />
  <br />
  <br />
  <auto-height-input></auto-height-input>
  <number-input></number-input>
</template>
<script lang="ts">
import { Options, Vue } from 'vue-class-component'
import MyinputDemo from '@/components/Myinput/Myinput.vue'
import AutoHeightInput from '@/components/Myinput/AutoHeightInput.vue'
import NumberInput from '@/components/Myinput/NumberInput.vue'

@Options({
  components: { MyinputDemo, AutoHeightInput, NumberInput }
})
export default class Myinput extends Vue {
  value = ''
  created(): void {}
}
</script>
