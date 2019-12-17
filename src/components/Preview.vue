<template>
  <div class="editor__preview" v-html="markdownText">
    {{ markdownText }}
  </div>
</template>

<script>

const marked = require('marked');

export default {

  props: ['text'],
  name: 'app',

  data() {
    return {
      test: '',
    };
  },
  computed: {
    markdownText() {
      return marked(this.text, { sanitize: true });
    },
  },
};
</script>
