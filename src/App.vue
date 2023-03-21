<template>
  <stored-movies :movieslist="movies"></stored-movies>
</template>

<script>
import StoredMovies from "./components/movies/StoredMovies.vue";

export default {
  components: {
    StoredMovies,
  },
  data() {
    return {
      movies: [
        {
          id: "menu",
          title: "Menu",
          description:
            "Młoda para wybiera się na odległą wyspę, do ekskluzywnej restauracji. Okazuje się jednak, że nie wszystko jest takie jakim się wydaje a w menu czekają zaskakujące niespodzianki.",
          link: "https://www.filmweb.pl/film/Menu-2022-875647",
        },
        {
          id: "bielmo",
          title: "Bielmo",
          description:
            "W 1830 roku Akademią Wojskową w West Point wstrząsa seria brutalnych morderstw. Weteran-detektyw i młody kadet prowadzą śledztwo.",
          link: "https://www.filmweb.pl/film/Bielmo-2022-870411",
        },
      ],
    };
  },
};
</script>

<style>
@import url("https://fonts.googleapis.com/css2?family=Jost&display=swap");
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
