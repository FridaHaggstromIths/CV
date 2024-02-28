<script setup>
import CvPortfolio from '../components/CvPortfolio.vue';
</script>


<template>
    <div id="wrapping">
      <div v-if="cv.length > 0">
        <div v-for="utbildning in cv" :key="utbildning.id">
          <div>
            <h5>{{ utbildning.Titel }}</h5>
            <p>{{ utbildning.Program }}</p>
            <p>{{ utbildning.År }}</p>
          </div>
        </div>
      </div>
      <div v-else>Loading...</div>
    </div>
    <CvPortfolio />
  </template>

  <script>
  export default {
    data() {
      return {
        cv: []
      }
    },
    created() {
      this.fetchData()
    },
    methods: {
      async fetchData() {
        try {
          const res = await fetch('Kompetenser.json')
          this.cv = await res.json()
        } catch (error) {
          console.error('Error fetching data:', error)
        }
      }
    }
  }
  </script>
