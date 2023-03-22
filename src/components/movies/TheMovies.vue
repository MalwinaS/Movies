<template>
  <base-card>
    <base-button
      @click="setSelectedTab('stored-movies')"
      :mode="storedResButtonMode"
      >Lista filmów</base-button
    >
    <base-button 
    @click="setSelectedTab('add-movie')" 
    :mode="addResButtonMode"
      >Dodaj film</base-button
    >
  </base-card>
  <component :is="selectedTab"></component>
</template>

<script>
import StoredMovies from "./StoredMovies.vue";
import AddMovie from "./AddMovie.vue";
export default {
  components: {
    StoredMovies,
    AddMovie,
  },
  data() {
    return {
      selectedTab: "stored-movies",
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
  computed: {
    storedResButtonMode() {
      return this.selectedTab === "stored-movies" ? null : "flat";
    },
    addResButtonMode() {
      return this.selectedTab === "add-movie" ? null : "flat";
    },
  },
  provide() {
    return {
      movieslist: this.movies,
    };
  },
  methods: {
    setSelectedTab(tab) {
      this.selectedTab = tab;
    },
  },
};
</script>
