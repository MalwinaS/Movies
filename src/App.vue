<template>
  <the-header title="Filmy do obejrzenia"></the-header>
  <the-movies></the-movies>
</template>

<script>
import TheHeader from "./components/layouts/TheHeader.vue";
import TheMovies from "./components/movies/TheMovies.vue";

export default {
  components: {
    TheHeader,
    TheMovies,
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Nunito:ital,wght@0,300;0,600;1,400;1,500&display=swap");
* {
  box-sizing: border-box;
}

html {
  font-family: "Jost", sans-serif;
}

body {
  margin: 0;
}
</style>
