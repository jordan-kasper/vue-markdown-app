<template>
  <div id="app container">
      <app-header></app-header>
      <app-editor></app-editor>
  </div>
</template>

<script>
import Editor from './components/Editor.vue';
import Header from './components/Header.vue';

export default {
  name: 'app',
  components: {
    appEditor: Editor,
    appHeader: Header,
  },
};
</script>

<style>
#app {
  margin-top: 60px;
}
.container{
  background-color: aqua;
}
html, body {
    max-width: 100%;
    overflow-x: hidden;
    overflow-y: hidden;
}
</style>
