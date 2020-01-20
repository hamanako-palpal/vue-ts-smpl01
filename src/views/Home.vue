<template>
  <div class="home">
    <Smpl :name="getText"></Smpl>
    <TextBox :messege="getText"></TextBox>
  </div>
</template>

<script lang="ts">
// @ is an alias to /src
import Smpl from '@/components/Smpl.vue';
import TextBox from '@/components/TextBox.vue';
import {Component, Vue} from 'vue-property-decorator';

@Component({
  components: {
    Smpl,
    TextBox,
  }
})

export default class Home extends Vue{

  public getText: string = "some";
}
</script>
