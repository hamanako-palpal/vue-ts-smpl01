<template>
  <div class="smpl">
    <img alt="Vue logo" src="../assets/logo.png">
    <Smpl msg="Welcome to Your Vue.js App"/>
  </div>
</template>

<script>
// @ is an alias to /src
import Smpl from '@/components/Smpl.vue'

export default {
  name: 'smpl',
  components: {
    Smpl
  }
}
</script>
