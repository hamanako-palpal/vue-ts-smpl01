<template>
  <div class="home">
    <Smpl :name="getText"></Smpl>
  </div>
</template>

<script lang="ts">
// @ is an alias to /src
import Smpl from '@/components/Smpl.vue';
import {Component, Vue} from 'vue-property-decorator';

@Component({
  components: {
    Smpl,
  }
})

export default class Home extends Vue{

  public getText: string = "some";
}
</script>
