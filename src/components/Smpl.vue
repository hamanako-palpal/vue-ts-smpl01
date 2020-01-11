<template>
  <button @click="onClick"> {{getName}}>>>>>{{getSome}}</button>
</template>

<script lang="ts">
import {Component, Vue} from 'vue-property-decorator';

@Component
export default class MyButton extends Vue{
  name = 'Button';
  some = false;
  get getName() {
    return this.name;
  }
  get getSome() {
    return this.some;
  }
  onClick() {
    this.some = true;
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
