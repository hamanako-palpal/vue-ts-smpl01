<template>
    <div class="home">
        <input type="text" ref="reftxt"/>
        <button @click="act">{{value}}</button>
    </div>
</template>

<script lang="ts">
  import {Component, Emit, Prop, Vue} from 'vue-property-decorator';

  @Component
  export default class TextBox extends Vue{

    @Prop() public value!: string;

    @Emit() public input(value: string) {}

    act() :void {
      var reft: HTMLInputElement = this.$refs.reftx as HTMLInputElement;
      this.input(reft.value);
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