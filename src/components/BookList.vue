<template>
    <div class="book-list">
        <BookItem v-for="book in books"
        :id="book.id"
        :title="book.title" 
        :author="book.author"
        :year="book.year" 
        :pages="book.pages"
        :cover="book.cover"
        :genre="book.genre"
        :description="book.description"
        :editorial="book.editorial"
        :language="book.language"
        :isbn="book.isbn"
        :price="book.price"
        :stock="book.stock"
        :favorite="book.favorite" 
        :rating="book.rating" 
        :personalNote="book.personalNote"/>
    </div>
</template>

<script >
import BookItem from './BookItem.vue'

export default {
    name: "",
    components:{
        BookItem
    },
    props:{
        books:{type:Array}
    },
    data(){
        return {
        }
    },
    methods: {
    }
}

</script>

<style>

.book-list {
padding: 20px;
display: grid;
grid-template-columns: repeat(2, 1fr);
grid-gap: 20px;
}

</style>