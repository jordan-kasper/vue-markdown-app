<template>
  <div class="editor">
    <textarea v-model="text" cols="30" rows="10" class="editor__input"></textarea>
    <app-preview :text="text"></app-preview>
  </div>
</template>

<script>
import Preview from './Preview.vue';

export default {
  name: 'app',
  data() {
    return {
      text: '',
    };
  },
  components: {
    appPreview: Preview,
  },
};
</script>

<style scoped>

</style>
