<template>
  <section class="nav-bar">
    <div class="nav-bar-container">

      <search-bar />

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

.nav-bar {
  background-color: #0d0f19;
  width: 400px;
  height: 100vh;
}
</style>