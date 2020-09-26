<template>
  <div class="home">
    <h1>{{ title }}</h1>
    <p>Movie Count: {{ movieCount }}</p>
  </div>
</template>

<script>
export default {
  name: "App",
  data() {
    return {
      title: "Vue Movies",
      movies: [
        {
          title: "Star Wars",
          poster:
            "https://images-na.ssl-images-amazon.com/images/I/81RZipc6yOL._AC_SL1500_.jpg",
        },
        {
          title: "Silence of the Lambs",
          poster:
            "https://images-na.ssl-images-amazon.com/images/I/410VHPrwUPL._AC_.jpg",
        },
        {
          title: "Ghostbusters",
          poster:
            "https://images-na.ssl-images-amazon.com/images/I/51Hdl8C50%2BL._AC_SL1023_.jpg",
        },
      ],
    };
  },
  watch: {
    // Used to watch when data changes, runs a function
  },
  computed: {
    // Used for getting computed state values
    // Goes OUTSIDE data()
    movieCount() {
      return this.movies.length;
    },
  },
  methods: {
    // place any functions or hooks here
  },
};
</script>

<style>
@import "./assets/global.css";

.home {
  display: flex;
  flex-direction: column;
  align-items: center;
  justify-content: center;
  padding: 20px;
}
</style>
