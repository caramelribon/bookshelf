<template>
  <div id="app">
    <shelf-header @add-book="onAddBook"></shelf-header>
    <shelf-message></shelf-message>
    <shelf-books :books="books"></shelf-books>
  </div>
</template>

<script>
import ShelfBooks from '@/components/ShelfBooks.vue';
import ShelfHeader from '@/components/ShelfHeader.vue';
import ShelfMessage from '@/components/ShelfMessage.vue';
import { getBooks } from '@/services/bookService';

export default {
  components: { ShelfBooks, ShelfHeader, ShelfMessage },
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
