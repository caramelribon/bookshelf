<template>
  <div id="app">
    <shelf-header @add-book="onAddBook"></shelf-header>
  </div>
</template>

<script>
import ShelfHeader from '@/components/ShelfHeader.vue';
import { getBooks } from '@/services/bookService';

export default {
  components: { ShelfHeader },
  data() {
    return { books: [] };
  },
  async created() {
    this.books = await getBooks()
      .catch((err) => {
        console.error(err.message);
        this.makeToast('エラーの発生', '書籍データを取得できませんでした。');
      });
  },
  methods: {
    makeToast(title, msg) {
      this.$bvToast.toast(msg, {
        autoHideDelay: 5000,
        title,
        variant: 'danger',
      });
    },
    onAddBook(book) {
      this.books.push(book);
    },
  },
};
</script>
