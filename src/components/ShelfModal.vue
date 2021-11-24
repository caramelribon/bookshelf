<template>
  <div>
    <b-button
      class="book-registration__show-btn"
      variant="outline-success"
      v-b-modal.book-registration
    >
      <b-icon-bookmark-plus></b-icon-bookmark-plus> 書籍の登録
    </b-button>
    <b-modal
      id="book-registration"
      hide-footer
      title="書籍の登録"
    >
    </b-modal>
  </div>
</template>

<script>
import {
  BButton,
  BIconBookmarkPlus,
  BModal,
  VBModal,
} from 'bootstrap-vue';

export default {
  components: {
    BButton,
    BIconBookmarkPlus,
    BModal,
  },
  directives: { 'b-modal': VBModal },
};
</script>

<style scoped>
.book-registration__show-btn {
  font-size: 1.2rem;
}
</style>
