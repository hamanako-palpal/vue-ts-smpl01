<template>
  <div>
    <!-- <input v-model="txt" placeholder={{ messege }}> -->
    <button @click="onClick">push</button>
  </div>
</template>

<script lang="ts">
import {Component, Prop, Vue} from 'vue-property-decorator';
import TextBox from '@/components/TextBox.vue';

@Component
export default class MyButton extends Vue{

  @Prop({default: ''}) name!: string;
  some = false;
  get getName() {
    return this.name;
  }
  get getSome() {
    return this.some;
  }
  onClick() {
    this.name += this.some; 
    this.some = !this.some;
    alert(this.name);
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
