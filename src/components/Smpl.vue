<template>
  <div class="home">
    <text-box v-model="myname"/>
    <h1>ttt {{ name }}</h1>
  </div>
</template>

<script lang="ts">
import {Component, Emit, Prop, Vue} from 'vue-property-decorator';
import TextBox from '@/components/TextBox.vue';

@Component({
  components: {TextBox},
})
export default class MyButton extends Vue {

  @Prop() name!: string;

  @Emit()
  public input(value: string) {}

  get myname() {
    return this.name;
  }

  set myname(value: string) {
    this.input(value);
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
