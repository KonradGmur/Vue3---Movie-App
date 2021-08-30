<template>
  <div class="home">
    <Hero />
  </div>
</template>

<script>
import axios from 'axios'
export default {
  data() {
    return {
      movies: [],
    }
  },
  methods: {
    async getMovies() {
      const data = axios.get(
        `https://api.themoviedb.org/3/search/movie?api_key=b0e7142d1912dc6e432dcfdb40d564fd&language=en-US&page=1&query=${this.searchInput}`
      )
      const result = await data
      console.log(result)
    },
  },
}
</script>
