<template>
  <div id="app">
    <shelf-header @add-book="onAddBook"></shelf-header>
  </div>
</template>

<script>
import ShelfHeader from '@/components/ShelfHeader.vue';

export default {
  components: { ShelfHeader },
  data() {
    return {books: []};
  },
  methods: {
    onAddBook(book) {
      this.books.push(book);
    },
  },
};
</script>
