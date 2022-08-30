/* eslint-disable */
<template>
  <div class="hello">
  
<Collapse
label="OPeN"
:view="open"
@toggle="open=!open"
>
 1<input>
 2<input>
 3<input>
 4<input>
  </Collapse>
  </div>
</template>

<script setup lang="ts">
import { defineComponent, ref } from 'vue';
import Collapse from '@/components/Collapse.vue';
let open = ref(false);
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped lang="scss">
h3 {
  margin: 40px 0 0;
}
ul {
  list-style-type: none;
  padding: 0;
}
li {
  display: inline-block;
  margin: 0 10px;
}
a {
  color: #42b983;
}
</style>
