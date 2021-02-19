<template>
  <div id="q-app">
    <router-view />
  </div>
</template>
<script lang="ts">
import { Vue, Component } from 'vue-property-decorator'

@Component
export default class App extends Vue {}
</script>

<style>
  #q-app{
    font-family: 'Lato', sans-serif;
    height: 100%;

  }
</style>
