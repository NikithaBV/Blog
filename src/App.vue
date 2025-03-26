<template>
  <div>
      <app-header></app-header>
      <router-view></router-view>
  </div>
</template>

<script>
// Imports

import headerAdd from './components/headerAdd.vue';

export default {
  components: {
      'app-header': headerAdd
  },
  data () {
      return {

      }
  },
  methods: {

  }
}
</script>

<style>
body{
  margin: 0;
  font-family: 'Nunito SemiBold';
}
</style>