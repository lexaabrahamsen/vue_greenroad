<template>
  <div class="home">
    <h1>{{ message }}</h1>
    <p>Here is a list of recycling centers {{ places }}</p>
  </div>
</template>

<style>
</style>

<script>
import axios from "axios";
export default {
  data: function() {
    return {
      message: "Green Roads",
      places: []
    };
  },
  created: function() {
    axios.get("/api/places").then(response => {
      console.log(response.data);
      this.places = response.data;
    });
  },
  methods: {}
};
</script>