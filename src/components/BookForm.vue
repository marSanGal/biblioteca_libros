<template>
    <div class="book-form">

        <form class="book-form__form">

            <div class="book-form__form-group">
                <label for="title">Title:</label>
                <input type="text" id="title" name="title">
            </div>

            <div class="book-form__form-group">
                <label for="author">Author:</label>
                <input type="text" id="author" name="author">
            </div>

            <div class="book-form__form-group">
                <label for="description">Description:</label>
                <textarea id="description" name="description"></textarea>
            </div>

            <div class="book-form__form-group">
                <label for="year">Year:</label>
                <input type="text" id="year" name="year">
            </div>

            <div class="book-form__form-group">
                <label for="pages">Pages:</label>
                <input type="text" id="pages" name="pages">
            </div>

            <div class="book-form__form-group">
                <label for="genre">Genre:</label>
                <input type="text" id="genre" name="genre">
            </div>

            <div class="book-form__form-group">
                <label for="editorial">Editorial:</label>
                <input type="number" id="editorial" name="editorial">
            </div>

            <div class="book-form__form-group">
                <label for="language">Language:</label>
                <input type="number" id="language" name="language">
            </div>

            <div class="book-form__form-group">
                <label for="isbn">ISBN:</label>
                <input type="number" id="isbn" name="isbn">
            </div>

            <div class="book-form__form-group">
                <label for="price">Price:</label>
                <input type="number" id="price" name="price">
            </div>

            <div class="book-form__form-group">
                <label for="stock">Stock:</label>
                <input type="number" id="stock" name="stock">
            </div>

            <div class="book-form__form-group">
                <label for="favorite">Favorite:</label>
                <input type="checkbox" id="favorite" name="favorite">
            </div>

            <div class="book-form__form-group">
                <label for="rating">Rating:</label>
                <input type="number" id="rating" name="rating" min="0" max="5">
            </div>

            <div class="book-form__form-group">
                <label for="image">Image:</label>
                <input type="number" id="image" name="image">
            </div>

            <div class="book-form__form-group">
                <button class="book-form__submit" type="submit">Add Book</button>
            </div>
        </form>
    </div>
</template>


<script>

</script>

<style>

h2 {
    text-align: left;
}

.book-form__form {
display: flex;
flex-wrap: wrap;
}

.book-form__form-group {
margin-bottom: 20px;
width: 50%;
display: flex;
flex-direction: column;
}

.book-form__form-group label {
display: block;
margin-bottom: 10px;
text-align: left;
font-size: 14px;
}

.book-form__form-group input,
.book-form__form-group textarea {
width: 80%;
padding: 10px;
border: 1px solid #e5e5e5;
border-radius: 4px;
outline: none;
text-align: left;
}

.book-form__form-group input:focus,
.book-form__form-group textarea:focus {
border-color: #000;
}

.book-form__form-group textarea {
height: 100px;
}

.book-form__submit {
padding: 10px;
border: 1px solid #e5e5e5;
border-radius: 4px;
outline: none;
cursor: pointer;
min-width: 100px;
background-color: #4caf50;
color: #fff;
}

.book-form__submit:hover {
background-color: #43a047;
}
</style>