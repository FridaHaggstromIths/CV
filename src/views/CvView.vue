<script setup>
import CvPortfolio from '../components/CvPortfolio.vue';
</script>


<template>
<div id="wrapping">
  <h3 id="Overview">Utbildning</h3>
      <div v-if="cv.Utbildning.length > 0">
        <div v-for="info in cv.Utbildning" :key="info.id">
          <div>
            <p>{{ info.Titel }}</p>
            <p>{{ info.Program }}</p>
            <p>{{ info.År }}</p>
          </div>
        </div>
      </div>
      <div v-else>Loading...</div>

  <h3 id="Overview">Kompetenser</h3>
      <div v-if="cv.Kompetenser.length > 0">
        <div v-for="info in cv.Kompetenser" :key="info.id">
          <div>
            <p>{{ info.Titel }}</p>
          </div>
        </div>
      </div>
      <div v-else>Loading...</div>

  <h3 id="Overview">Arbete</h3>
      <div v-if="cv.Arbete.length > 0">
        <div v-for="info in cv.Arbete" :key="info.id">
          <div>
            <p>{{ info.Arbetsgivare }}</p>
            <p>{{ info.Titel }}</p>
            <p>{{ info.Arbete }}</p>
            <p>{{ info.År }}</p>
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


<style>
#wrapping {
        position: absolute; /* Absolut positionering relativt till första föräldern med relativ eller absolut positionering */
        top: 50%;           /* Centrerar vertikalt till % av förälderns höjd */
        left: 60%;          /* Centrerar horisontellt till % av förälderns bredd */
        transform: translate(-50%, -50%); /* Justerar positionen så att centrum av elementet hamnar exakt i mitten */
        color: #3d2636;
        font-size:large;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        height: 80vh;
    }

</style>
