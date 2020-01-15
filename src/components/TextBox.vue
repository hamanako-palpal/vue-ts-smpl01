<template>
    <div>
        <input v-model="message" placeholder="edit me">
        <p>Message is: {{ message }}</p>
    </div>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator';
import { watch } from 'fs';

@Component
export default class TextBox extends Vue{
  text = '';
  @watch('text')
  private change(val: string, oldVal: string) {
      
  }

}
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
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