<template>
  <div id="app">
    <div class="container">
      <app-header></app-header>
      <app-editor></app-editor>
    </div>
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

</style>
