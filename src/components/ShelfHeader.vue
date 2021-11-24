<template>
  <b-container>
    <b-row>
      <b-col>
        <b-navbar>
          <b-navbar-brand href="./index.html">
            <img
              src="@/assets/logo.png"
              alt="Bookshelf"
            />
          </b-navbar-brand>
        </b-navbar>
      </b-col>
    </b-row>
  </b-container>
</template>

<script>
import {
  BCol,
  BContainer,
  BNavbar,
  BNavbarBrand,
  BRow,
} from 'bootstrap-vue';

export default {
  components: {
    BCol,
    BContainer,
    BNavbar,
    BNavbarBrand,
    BRow,
  },
};
</script>
