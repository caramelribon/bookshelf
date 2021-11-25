<template>
  <b-container
    class="shelf-books"
    role="main"
  >
    <b-row>
      <b-col v-if="books.length === 0">
        <p class="text-center">登録された本はありません。</p>
      </b-col>
      <b-col
        v-for="book in books"
        :key="book.id"
        class="my-3"
        cols="6"
        md="4"
        lg="3"
      >
        <pre class="shelf-books__item">{{ JSON.stringify(book, null, 2) }}</pre>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import {
  BCol,
  BContainer,
  BRow,
} from 'bootstrap-vue';

export default {
  components: {
    BCol,
    BContainer,
    BRow,
  },
  props: {
    books: {
      type: Array,
      required: true,
    },
  },
};
</script>

<style scoped>
.shelf-books__item {
  background-color: #fafafa;
}
</style>
