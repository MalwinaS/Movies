<template>
  <ul>
    <movie-list
      v-for="movie in movieslist"
      :key="movie.id"
      :id="movie.id"
      :title="movie.title"
      :description="movie.description"
      :link="movie.link"
    ></movie-list>
  </ul>
</template>

<script>
import MovieList from "./MovieList.vue";
export default {
  components: {
    MovieList,
  },
  inject: ["movieslist"],
};
</script>

<style scoped>
ul {
  list-style: none;
  margin: 0;
  padding: 0;
  margin: auto;
  max-width: 40rem;
}
</style>
