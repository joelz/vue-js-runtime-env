<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <div>API Base: {{ apiBase }}</div>
    <div>{{ variable1 }}</div>
  </div>
</template>

<script>
import { getEnv } from '@/utils/index'

export default {
  name: 'App',
  data() {
    return {
      variable1: getEnv('VUE_APP_VARIABLE_1'),
      apiBase: getEnv('VUE_APP_BASE_API')
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
