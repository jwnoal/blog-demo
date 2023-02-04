<template>
  <div>Lodash.js</div>
  <div>{{ arr }}</div>

  <div>
    chunk: 分组<br />
    Lodash.chunk(arr, 3) <br />
    {{ arr_chunk }}
  </div>

  <div>
    compact: 过滤假值<br />
    Lodash.compact(arr) <br />
    {{ arr_compact }}
  </div>

  <div>
    concat: 连接数组<br />
    Lodash.concat(arr, 2, [3], [[4]]) <br />
    {{ arr_concat }}
  </div>
</template>
<script setup lang="ts">
import Lodash from 'lodash'
// import { ref } from 'vue'
const arr = [1, , 0, undefined, 2, 3, 4, 5, 6, 7, 8]
const arr_chunk = Lodash.chunk(arr, 3)
const arr_compact = Lodash.compact(arr)
const arr_concat = Lodash.concat(arr, 2, [3], [[4]])
</script>
<style lang="less" scoped>
div {
  margin-bottom: 20px;
}
</style>
