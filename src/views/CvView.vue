<script setup>
/* import CvPortfolio from '../components/CvPortfolio.vue'; */
</script>


<template>
<div class="Wrapping">
  <h3 id="Utbildning">Utbildning</h3>
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
<!--
      <h3 id="Overview">Kompetenser</h3> -->
  <h3 id="Kompetenser">Kompetenser</h3>
      <div v-if="cv.Kompetenser.length > 0">
        <div v-for="info in cv.Kompetenser" :key="info.id">
          <div>
            <p>{{ info.Titel }}</p>
          </div>
        </div>
      </div>
      <div v-else>Loading...</div>

  <h3 id="Arbete">Arbete</h3>
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
  <!-- <CvPortfolio /> -->
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
/* #wrapping {
        color: #3d2636;
        font-size:large;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
        display: flex;
        flex-direction: column;
        min-height: 100vh;
        margin-top: 5vh;
        margin-bottom: 5vh;
        justify-content: center;
        align-items: center;
        width: 600px;
        margin:0 auto;


    } */

/* Grid Container */
.Wrapping {
  display: grid;
  height: 100vh;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows:

    /* NAV */
    /* 1fr */
    /* item1 */
    1fr;
    /*item2*/
    /* 1fr */
    /* item3 */
   /*  1fr; */

    grid-template-areas:
    /* "nav nav" */
    "item3 item4 item5";
    /* "item1 item2"; */
    /* "footer"; */

}

#Utbildning{
  display: grid;
  grid-area: item3;
  justify-items: center;
  align-items: start;
  margin-top: 5vh;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

#Kompetenser{
  display: grid;
  grid-area: item4;
  justify-items: center;
  align-items: start;
  margin-top: 5vh;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}


#Arbete{
  display: grid;
  grid-area: item5;
  justify-items: center;
  align-items: start;
  margin-top: 5vh;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

p{
  display: grid;
  justify-items: center;
  align-items: end;
  width: 30vh;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}
</style>
