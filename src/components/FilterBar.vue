<template>

<div class="filter-bar">

    <div class="filter-bar__select">
        <label for="sort-by">Sort by:</label>

        <select id="sort-by">
            <option value="title">Title</option>
            <option value="author">Author</option>
            <option value="year">Year</option>
            <option value="rating">Rating</option>
        </select>
    </div>

    <div class="filter-bar__select">
        <label for="sort-order">Sort by:</label>
        <select id="sort-order">
            <option value="asc">Ascending</option>
            <option value="desc">Descending</option>
        </select>
    </div>

    <div class="filter-bar__check">
        <label for="favorites">Favorites:</label>
        <input type="checkbox" id="favorites" v-model="showFavorites">
    </div>

</div>

</template>

<script >
export default {
data() {
    return {
        showFavorites: false,
        };
    },
};
</script>

<style>

.filter-bar {
display: flex;
align-items: center;
padding: 20px;
background-color: #f5f5f5;
border-bottom: 1px solid #ccc;
}
.filter-bar__select {
display: flex;
align-items: center;
margin-right: 20px;
}
.filter-bar__select label {
margin-right: 10px;
}
.filter-bar__select select {
padding: 10px;
border: 1px solid #ccc;
border-radius: 4px;
outline: none;
}
.filter-bar__check {
display: flex;
align-items: center;
}
.filter-bar__check input {
margin-right: 10px;
}
.filter-bar__check label {
cursor: pointer;
}

</style>
