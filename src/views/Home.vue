<template>
  <div class="home">
    
    <h1>{{ message }}</h1>
    <h2>Getting rid of our plastic waste, one road at a time.</h2>
    <br>
    <p>Search for your closest Recycling Center</hp>
    <p><input type="text" v-model="searchTerm"></p>
    <!--THIS WILL SHOW THE INDEX OF ALL REC PLACES <p>Find your closest recycling center! {{ places }}</p> -->
    <div v-for="place in filterBy(places, searchTerm, 'address')">
    <br>
    <h2>{{ place.name }}</h2>
    <p>{{ place.address }}</p>
    <p>{{ place.hours }}</p>
    <p>{{ place.distance }} mi</p>
    </div>
  </div>
</template>


<style>
</style>


<script>
import axios from "axios";
import Vue2Filters from "vue2-filters";

export default {
  mixins: [Vue2Filters.mixin],
  data: function() {
    return {
      message: "Green Roads",
      places: [],
      searchTerm: ""
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