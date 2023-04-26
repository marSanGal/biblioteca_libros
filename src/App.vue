<template>
  <div class="app">

    <header class="header">
      <img class="logo" src="./assets/uoc-logo.png" alt="Logo">
      <h1 class="title">Book Manager</h1>
    </header>

    <div class="content">
      <SearchBar />
      <FilterBar />

      <main class="main">
        <BookList :books="books" />
      </main>

      <ModalLayer v-if="showModal" name="Add new book">
        <BookForm />
      </ModalLayer>
    </div>

  </div>
</template>

<script>
import SearchBar from './components/SearchBar.vue';
import FilterBar from './components/FilterBar.vue';
import BookList from './components/BookList.vue';
import ModalLayer from './components/ModalLayer.vue';
import BookForm from './components/BookForm.vue';

export default {
  name: 'App',
  components: {
    SearchBar,
    FilterBar,
    BookList,
    ModalLayer,
    BookForm,
  },
  data() {
    return {
      showModal: false,
      books: [
        {
          id: 1,
          title: "Rebecca",
          author: "Daphne du Maurier",
          year: 1938,
          pages: 464,
          cover: "https://imagessl0.casadellibro.com/a/l/t5/60/9788497938860.jpg",
          genre: "Novela Gótica",
          description: "Anoche soñe que volvía a Manderley... Así comienzan los recuerdos de la segunda señora De Winter, que la transportan de nuevo a la aislada y gris mansión situada en la húmeda y ventosa costa de Cornualles. Con un marido al que apenas conoce, la joven esposa llega a este inmenso predio para ser inexorablemente ahogada por la fantasmal presencia de la primera señora De Winter, la hermosa Rebeca, muerta pero nunca olvidada. Su habitación permanece intacta, sus vestidos listos para ser lucidos y su sirvienta, la siniestra señora Danvers, aún le profesa una devoción malsana.",
          editorial: "Debolsillo",
          language: "Spanish",
          isbn: 9788497938860,
          price: 9.45,
          stock: 35,
          favorite: true,
          rating: "5/5",
          personalNote: "Lorem fistrum tiene musho peligro te va a hasé pupitaa a gramenawer te voy a borrar el cerito quietooor mamaar por la gloria de mi madre fistro.",
        },
        {
          id: 2,
          title: "Pet Sematary",
          author: "Stephen King",
          year: 1983,
          pages: 488,
          cover: "https://www.dreamofhome.co.uk/wp-content/uploads/2018/04/pet-sematary-1.jpg",
          genre: "Terror",
          description: "Louis lo había comprobado: el gato estaba muerto, y por eso lo había enterrado. Aun así, incomprensiblemente, el gato había vuelto a casa. Church estaba allí otra vez, como Louis Creed temía y deseaba. Porque su hijita Ellie le había encomendado que cuidara del gato, y Church había muerto atropellado. Louis lo había comprobado: el gato estaba muerto, incluso lo había enterrado más allá del cementerio de animales. Sin embargo, Chruch había regresado, y sus ojos eran más crueles y perversos que antes. Pero volvía a estar allí y Ellie no lo lamentaría.",
          editorial: "Debolsillo",
          language: "Spanish",
          isbn: 9788466357333,
          price: 11.35,
          stock: 17,
          favorite: true,
          rating: "4.5/5",
          personalNote: "Lorem fistrum tiene musho peligro te va a hasé pupitaa a gramenawer te voy a borrar el cerito quietooor mamaar por la gloria de mi madre fistro.",
        },
        {
          id: 3,
          title: "In Their Shoes: Navigating Non-Binary Life",
          author: "Jamie Windust",
          year: 2020,
          pages: 208,
          cover: "https://cdn.waterstones.com/bookjackets/large/9781/7877/9781787752429.jpg",
          genre: "LGBTQ+",
          description: "There is no one way to be non-binary, and that's truthfully one of the best things about it. It's an identity that is yours to shape. Frank, funny, and brilliantly feisty, this must-read book is a call to arms for non-binary self-acceptance, self-appreciation and self-celebration.",
          editorial: "Jessica Kingsley Publishers",
          language: "English",
          isbn: 9781787752429,
          price: 12.99,
          stock: 35,
          favorite: false,
          rating: "3.5/5",
          personalNote: "Lorem fistrum tiene musho peligro te va a hasé pupitaa a gramenawer te voy a borrar el cerito quietooor mamaar por la gloria de mi madre fistro.",
        },
        {
          id: 4,
          title: "Stage Ghosts and Haunted Theatres",
          author: "Nick Bromley",
          year: 2021,
          pages: 224,
          cover: "https://m.media-amazon.com/images/I/51bCkYVWcAL._SX329_BO1,204,203,200_.jpg",
          genre: "Ghosts & Poltergeists",
          description: "STAGE GHOSTS AND HAUNTED THEATRES will take you on a spectral visit to other 50 theatres in the UK from the relative safety of your armchair.",
          editorial: "LPN Books",
          language: "English",
          isbn: 957268319,
          price: 9.99,
          stock: 4,
          favorite: false,
          rating: "4.5/5",
          personalNote: "Lorem fistrum tiene musho peligro te va a hasé pupitaa a gramenawer te voy a borrar el cerito quietooor mamaar por la gloria de mi madre fistro.",
        },
      ],
    };
  },
};
</script>

<style>

body {
padding: 0;
margin: 0;
font-family: "Avenir", Helvetica, Arial, sans-serif;
-webkit-font-smoothing: antialiased;
-moz-osx-font-smoothing: grayscale;
text-align: center;
color: #2c3e50;
}
.header {
display: flex;
align-items: center;
padding: 0 20px;
background-color: #f5f5f5;
border-bottom: 1px solid #e5e5e5;
}
.header__left {
display: flex;
align-items: center;
}
.logo {
height: 40px;
margin-right: 10px;
}
.title {
font-size: 24px;
font-weight: 400;
}

</style>

