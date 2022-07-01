<template>
  <section class="nav-bar">
    <div class="nav-bar-container">

      <!-- <search-bar /> -->

  <div class="nav-bar-icons">

<div class="nav-bar-home">
      <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="currentColor" class="bi bi-grid-3x3-gap-fill" viewBox="0 0 16 16">
  <path d="M1 2a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1V2zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1V2zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1V2zM1 7a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1V7zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1V7zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1V7zM1 12a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H2a1 1 0 0 1-1-1v-2zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1H7a1 1 0 0 1-1-1v-2zm5 0a1 1 0 0 1 1-1h2a1 1 0 0 1 1 1v2a1 1 0 0 1-1 1h-2a1 1 0 0 1-1-1v-2z"/>
</svg>
<!-- <h3 class="nav-bar-home-heading">FEED</h3> -->

</div>

  <svg xmlns="http://www.w3.org/2000/svg" width="30" height="30" fill="currentColor" class="bi bi-film" viewBox="0 0 16 16">
  <path d="M0 1a1 1 0 0 1 1-1h14a1 1 0 0 1 1 1v14a1 1 0 0 1-1 1H1a1 1 0 0 1-1-1V1zm4 0v6h8V1H4zm8 8H4v6h8V9zM1 1v2h2V1H1zm2 3H1v2h2V4zM1 7v2h2V7H1zm2 3H1v2h2v-2zm-2 3v2h2v-2H1zM15 1h-2v2h2V1zm-2 3v2h2V4h-2zm2 3h-2v2h2V7zm-2 3v2h2v-2h-2zm2 3h-2v2h2v-2z"/>
</svg>


<svg xmlns="http://www.w3.org/2000/svg" width="35" height="35" fill="currentColor" class="bi bi-tv" viewBox="0 0 16 16">
  <path d="M2.5 13.5A.5.5 0 0 1 3 13h10a.5.5 0 0 1 0 1H3a.5.5 0 0 1-.5-.5zM13.991 3l.024.001a1.46 1.46 0 0 1 .538.143.757.757 0 0 1 .302.254c.067.1.145.277.145.602v5.991l-.001.024a1.464 1.464 0 0 1-.143.538.758.758 0 0 1-.254.302c-.1.067-.277.145-.602.145H2.009l-.024-.001a1.464 1.464 0 0 1-.538-.143.758.758 0 0 1-.302-.254C1.078 10.502 1 10.325 1 10V4.009l.001-.024a1.46 1.46 0 0 1 .143-.538.758.758 0 0 1 .254-.302C1.498 3.078 1.675 3 2 3h11.991zM14 2H2C0 2 0 4 0 4v6c0 2 2 2 2 2h12c2 0 2-2 2-2V4c0-2-2-2-2-2z"/>
</svg>



  </div>


    </div>
  </section>
</template>

<script>
import SearchBar from '../SearchBar/SearchBar.vue'

export default {
  name: 'NavBar',
  
  components: {
    SearchBar
  }
}
</script>

<style lang="scss" scoped>
@import 'assets/scss/_color-palette.scss';
@import url('https://fonts.googleapis.com/css2?family=Manrope:wght@800&display=swap');

.nav-bar {
  // background-color: #0d0f19;
  background-color: colorPaletteSetting(primary);
  width: 120px;
  height: 100vh;
  font-family: 'Manrope', sans-serif;
  border-radius: 30px;


  &-icons {
    display: flex;
    justify-content: space-evenly;
    align-items: center;
    flex-direction: column;
    height: 300px;
    width: 100%;
  }

  &-home {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: colorPaletteSetting(secondary);
    width: 100px;
    height: 50px;
    border-radius: 10px;
    // border-bottom: 1px colorPaletteSetting(core-dark-grey) solid;
    cursor: pointer;
  }

  &-home-heading {
    color: white;
    padding-left: 20px;
  }
}

.bi-film {
  color: colorPaletteSetting(core-white);
  cursor: pointer;
}

.bi-grid-3x3-gap-fill {
  // color: colorPaletteSetting(core-white);
  color: colorPaletteSetting(tertiary);
}

.bi-tv {
  color: colorPaletteSetting(core-white);
  cursor: pointer;
}
</style>