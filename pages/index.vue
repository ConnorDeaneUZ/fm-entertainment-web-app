<template>
<section class="homepage-container">

  <nav-bar />
  
  <div class="movies-container">

  <movie-card v-for="movie in movies" :key="movie.index"
  :title="movie.title"
  :year="movie.year"
  :rating="movie.rated"
  :genre="movie.genre[0]"
  :poster="movie.poster"
  />

  </div>
</section>
</template>

<script>
import MovieCard from '../components/Global/MovieCard/MovieCard.vue'
import NavBar from '../components/Global/NavBar/NavBar.vue'
import movies from '~/config/movies'

export default {
  name: 'IndexPage',

  components: {
    MovieCard,
    NavBar
  },

  data: () => ({
    movies: movies.movies
  })
}
</script>

<style lang="scss">
@import 'assets/scss/_color-palette.scss';
 body {
  margin: 0 !important;
  padding: 0 !important;
  box-sizing: border-box !important;
}

.movies-container {
  display: grid;
  grid-template-columns: repeat(4,150px);  /* 3 columns */
  grid-template-rows: repeat(4,150px); /* 3 rows  */
  grid-gap:100px 300px; /* 50 pixels of space added between rows and 30 pixels added between columns  */
}

.homepage-container {
  background-color: colorPaletteSetting(tertiary);
  display: flex;
  height: 100vh;
}
</style>
