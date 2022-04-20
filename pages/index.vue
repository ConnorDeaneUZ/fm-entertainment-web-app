<template>
<section class="homepage-container">

  <movie-card v-for="movie in movies" :key="movie.index"
  :title="movie.title"
  :year="movie.year"
  :rating="movie.rated"
  :genre="movie.genre[0]"
  :poster="movie.poster"
  />

</section>
</template>

<script>
import MovieCard from '../components/Global/MovieCard/MovieCard.vue'

export default {
  name: 'IndexPage',

  components: {
    MovieCard
  },

  data: () => ({
    movies: [
    {
      title: "Spiderman: No Way Home",
      year: "2019",
      rated: "15",
      runtime: "106 min",
      genre: ['action', 'sci-fi'],
      poster: "https://m.media-amazon.com/images/M/MV5BZWMyYzFjYTYtNTRjYi00OGExLWE2YzgtOGRmYjAxZTU3NzBiXkEyXkFqcGdeQXVyMzQ0MzA0NTM@._V1_FMjpg_UX1000_.jpg",
    },
    {
      title: "The Batman",
      year: "2022",
      rated: "18",
      runtime: "180 min",
      genre: ['action', 'noir', 'thriller'],
      poster: "https://m.media-amazon.com/images/M/MV5BOGE2NWUwMDItMjA4Yi00N2Y3LWJjMzEtMDJjZTMzZTdlZGE5XkEyXkFqcGdeQXVyODk4OTc3MTY@._V1_.jpg",
    },
    {
      title: "Texas Chainsaw Massacre",
      year: "2022",
      rated: "18",
      runtime: "90 min",
      genre: ['horror'],
      poster: "https://m.media-amazon.com/images/M/MV5BNjVhZTkxMzgtM2M1NS00NjJkLTllYjUtMzQ5Y2IxNmE4OTFlXkEyXkFqcGdeQXVyMTEyMjM2NDc2._V1_.jpg",
    },
    {
      title: "James Bond: No Time To Die",
      year: "2021",
      rated: "12A",
      runtime: "163 min",
      genre: ['action'],
      poster: "https://static.posters.cz/image/1300/james-bond-no-time-to-die-azure-teaser-i84058.jpg",
    },
    {
      title: "The Boys: Season One",
      year: "2019",
      rated: "18",
      runtime: "60 min",
      genre: ['drama'],
      poster: "https://m.media-amazon.com/images/M/MV5BNGEyOGJiNWEtMTgwMi00ODU4LTlkMjItZWI4NjFmMzgxZGY2XkEyXkFqcGdeQXVyNjcyNjcyMzQ@._V1_.jpg",
    },
  ]
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

.homepage-container {
  justify-content: center;
  display: grid;
  grid-template-rows: 300px 300px 300px;
  grid-template-columns: 450px 450px 450px;
  background-color: colorPaletteSetting(primary);
  height: 100vh;
}
</style>
