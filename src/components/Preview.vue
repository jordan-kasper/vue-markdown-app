<template>
  <div v-html="markdownText">
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
    /**
     * renders the prop text to HTML based off the markdown that is passed.
     */
    markdownText() {
      marked.setOptions({
        renderer: new marked.Renderer(),
        gfm: true,
        tables: true,
        breaks: true,
        pedantic: false,
        sanitize: true,
        smartLists: true,
        smartypants: false,
      });
      return marked(this.text);
    },
  },
};
</script>

<style scoped></style>
