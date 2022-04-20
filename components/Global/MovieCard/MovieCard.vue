<template>
  <section class="movie-card">
    <div class="movie-card-container" :style="`background-image: url(${poster})`">
      
      <div class="movie-card-watch">
        <p>Watch Now</p>
      </div>
      
      <div class="movie-card-bottom">
        <div class="movie-card-bottom-info">
          <p>{{year}}</p>
          <p>{{rating}}</p>
          <p>{{genre}}</p>
        </div>
        <div class="movie-card-bottom-title">
          <p class="movie-title">{{title}}</p>
        </div>
      </div>
    </div>
  </section>
</template>

<script>
export default {
  name: 'MovieCard',

  props: {
    title: {
      type: String,
      required: true
    },
    year: {
      type: String,
      required: true
    },
    genre: {
      type: String,
      required: true
    },
    rating: {
      type: String,
      required: true
    },
    poster: {
      type: String,
      required: true
    }
  }
}
</script>

<style lang="scss" scoped>
@import url('https://fonts.googleapis.com/css2?family=Manrope:wght@800&display=swap');
@import 'assets/scss/_color-palette.scss';

.movie-card {
  font-family: 'Manrope', sans-serif;
  padding: 20px;

  &-container {
    position: relative;
    display: flex;
    justify-content: flex-end;
    flex-direction: column;
    width: 400px;
    height: 200px;
    // background-color: red;
    background-position: bottom;
    background-size: cover;
    background-repeat: no-repeat;
    border-radius: 5px;
    cursor: pointer;
    box-shadow: rgba(0, 0, 0, 0.16) 0px 3px 6px, rgba(0, 0, 0, 0.23) 0px 3px 6px;

    &:before {
    content: '';
    position: absolute;
    bottom: 0;
    left: 0;
    height: 80%;
    width: 100%;
    background: linear-gradient(to bottom, rgba(0,0,0,0) 0%,rgba(0,0,0,0.2) 50%,rgba(0,0,0,1) 100%);
    z-index: 1;
    transition: height 0.4s ease-out;
    }
  }

  &-container:hover {
    &:before {
      height: 100%;
      transition: height 0.4s ease-out;
      background: linear-gradient(to bottom, rgba(0,0,0,0) 0%,rgba(0,0,0,0.8) 50%,rgba(0,0,0,1) 100%);
    }

    .movie-card-watch {
      display: flex;
    }
  }

  &-bottom {
    // background-color: blue;
    width: 100%;
    height: 60px;
    z-index: 3;
  }

  &-bottom-info {
    display: flex;
    justify-content: space-evenly;
    color: colorPaletteSetting(core-light-grey);
    // background-color: green;
    height: 20px;
    width: 120px;
    align-items: center;
    font-size: 12px;
    margin-left: 20px;
  }

  &-bottom-title {
    display: flex;
    color: colorPaletteSetting(core-white);
    height: 40px;
    font-size: 18px;
    align-items: center;
    margin-left: 30px;
  }

  &-watch {
    justify-content: center;
    position: relative;
    font-size: 25px;
    color: white;
    z-index: 4;
    display: none;
  }

}
</style>