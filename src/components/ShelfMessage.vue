<template>
  <b-jumbotron
    class="shelf-message text-center"
    header="Bookshelf"
    lead="カンタン！あなたのオンライン本棚"
    text-variant="white"
  >
  </b-jumbotron>
</template>

<script>
import { BJumbotron } from 'bootstrap-vue';

export default { components: { BJumbotron } };
</script>

<style scoped>
.shelf-message {
  background-image: url('~@/assets/cover.jpg');
}

.shelf-message h1 {
  font-family: serif;
}
</style>
