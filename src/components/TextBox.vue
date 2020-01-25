<template>
    <div class="home">
        <input type="text" v-model="value"/>
        <button @click="act">{{this.btnname}}</button>
    </div>
</template>

<script lang="ts">
  import {Component, Emit, Prop, Vue} from 'vue-property-decorator';

  @Component
  export default class TextBox extends Vue{

    private value!: string;

    @Prop({default: 'aso'}) private btnname!: string;

    @Emit() public input(value: string) {}

    get val(): string {
      return this.btnname;
    }

    act() :void {

      var t = this.value;
      this.value = "";

      this.input(t);
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