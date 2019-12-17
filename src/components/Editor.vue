<template>
  <div class="container">
    <div class="row">
      <div class="input">
        <h2 class="text-center">Enter Markdown Text</h2>
        <textarea
          style="height:auto"
          rows="38"
          class="form-control"
          v-model="text"
        ></textarea>
      </div>
      <div id="preview">
        <h2 class="text-center">Preview</h2>
        <app-preview :text="text" class="output"></app-preview>
      </div>
    </div>
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
.output{
  padding: 20px;
  overflow-y:auto;
  height: 925px;
}
.input{
  height: 925px;
  width: 500px;
}
</style>
