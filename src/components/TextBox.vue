<template>
    <div class="home">
        <input type="text" v-model="txt"/>
        <button @onClick="act">tt</button>
    </div>
</template>

<script lang="ts">
  import {Component, Emit, Prop, Vue} from 'vue-property-decorator';

  @Component
  export default class TextBox extends Vue{

    @Prop() public value!: string;

    @Emit() public input(value: string) {}

    private get txt(): string {
      return this.value;
    }

    private set txt(value: string) {
      this.input(value);
    }

    act() :void {
      this.input("ioioio");
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