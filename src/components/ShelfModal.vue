<template>
  <div>
    <b-button
      class="book-registration__show-btn"
      variant="outline-success"
    >
      <b-icon-bookmark-plus></b-icon-bookmark-plus> 書籍の登録
    </b-button>
  </div>
</template>

<script>
import {
  BButton,
  BIconBookmarkPlus,
} from 'bootstrap-vue';

export default {
  components: {
    BButton,
    BIconBookmarkPlus,
  },
};
</script>

<style scoped>
.book-registration__show-btn {
  font-size: 1.2rem;
}
</style>
