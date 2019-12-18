<template>
  <div>
    <div class="row">
      <div class="col-md-6 input">
        <h2 class="text-center">Enter Markdown Text</h2>
        <textarea
          style="height:auto"
          rows="37"
          class="form-control"
          v-model="text"
        ></textarea>
      </div>
      <div class="col-md-6 output">
        <h2 class="text-center">Preview</h2>
        <app-preview :text="text" class="output-display"></app-preview>
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
  padding-top: 100px;
  padding-left: 50px;
  height: 900px;
  padding-right: 0px;

}
.output-display{
  overflow-y:auto;
  height: 925px;
}
.input{
  padding-top: 100px;
  padding-left: 50px;
  padding-right: 0px;
}
</style>
