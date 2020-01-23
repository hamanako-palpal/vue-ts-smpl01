<template>
  <div class="home">
    <text-box v-model="myname"/>
    <ul id="aso">
      <li v-for="item in mylist">
        <p>{{item}}</p><br>
      </li>
    </ul>
  </div>
</template>

<script lang="ts">
import {Component, Emit, Prop, Vue} from 'vue-property-decorator';
import TextBox from '@/components/TextBox.vue';

@Component({
  components: {TextBox},
})
export default class Smpl extends Vue {

  list: string[] = [];

  @Prop() value!: string;

  @Emit() public input(value: string) {}

  get myname() {
    this.list.push(this.value);
    return this.value;
  }

  set myname(value: string) {
    this.input(value);
  }

  get mylist() {
    return this.list;
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
