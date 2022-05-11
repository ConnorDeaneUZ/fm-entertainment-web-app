<template>
  <section class="search-bar">
    <div class="search-bar-container">
      
      <input class="search" type="text" placeholder="Search">
    </div>

  </section>
</template>

<script>
export default {
  name: 'SearchBar'
}
</script>

<style lang="scss" scoped>
.search-bar {
  display: flex;
  justify-content: center;
  align-items: center;
  width: 100%;
  height: 100px;
}

.search {
  width: 250px;
  height: 15px;
  border-radius: 100px;
  border: none;
  font-size: 18px;
  padding: 15px;
  outline: none;
}

</style>