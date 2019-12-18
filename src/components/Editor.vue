<template>
  <!-- eslint-disable max-len -->
  <!-- eslint-operator-linebreak -->

  <div>
    <div class="row">
      <div class="col-md-6 input">
        <h2 class="text-center">Enter Markdown Text</h2>
        <textarea
          style="height:auto"
          rows="37"
          class="form-control"
          v-model="text"
        >
        </textarea>
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
      text:
        '# H1 header\n'
        + 'Paragraphs are separated by a blank line.\n'
        + '2nd paragraph. *Italic*, **bold**, and `monospace`. Itemized lists \n'
        + 'look like: \n'
        + '* this one \n'
        + '* that one \n'
        + '* the other one \n'
        + ' \n'
        + 'Note that --- not considering the asterisk --- the actual text content starts at 4-columns in. \n'
        + '> Block quotes are \n'
        + '> written like so. \n'
        + '> \n'
        + '> They can span multiple paragraphs, \n'
        + '> if you like. \n'
        + ' \n'
        + 'As you probably guessed, indented 4 spaces. By the way, instead of indenting the block, \n'
        + 'you can use delimited blocks, if you like: \n'
        + '~~~ \n'
        + 'define foobar() { \n'
        + 'print "Welcome to flavor country!"; \n'
        + '} \n'
        + '~~~ \n',
    };
  },
  components: {
    appPreview: Preview,
  },
};
</script>

<style scoped>
.output {
  padding-top: 100px;
  padding-left: 50px;
  height: 900px;
  padding-right: 0px;
}
.output-display {
  overflow-y: auto;
  height: 925px;
}
.input {
  padding-top: 100px;
  padding-left: 50px;
  padding-right: 0px;
}
</style>
