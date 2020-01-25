<template>
  <div class="home">
    <text-box :btnname="sendname" @input="ipt => myname(ipt)"/>
    <ul v-for="item in mylist">
      <li>{{item}}</li>
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

  @Prop() private value!: string;

  // @Emit() public input(value: string) {}

  public sendname: string =this.value;
  

  public myname(ipt: string) {
    this.list.push(ipt);
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
