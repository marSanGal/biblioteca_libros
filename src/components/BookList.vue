import BookItem from './BookItem.vue';

<template>
  <div class="book-list">
    <BookItem v-for="book in books" :book="book" @delete-book="onDeleteBook" />
  </div>
</template>

<script>
import BookItem from "./BookItem.vue";
export default {
  name: "BookList",
  components: {
    BookItem,
  },
  props: {
    books: {
      type: Array,
      required: true,
    },
  },
  methods: {
    onDeleteBook(id) {
      // Emitir el evento "delete-book" con el identificador del libro a eliminar
      this.$emit('delete-book', id);
    }
  }
};
</script>

<style>
.book-list {
  padding: 20px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 20px;
}
</style>
