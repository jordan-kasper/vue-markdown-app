<template>
  <div id="app">
    <img alt="Vue logo" src="./assets/logo.png">
    <app-editor></app-editor>

  </div>
</template>

<script>
import Editor from './components/Editor.vue';

export default {
  name: 'app',
  components: {
    appEditor: Editor,
  },
};
</script>

<style>
#app {
  font-family: 'Avenir', Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
