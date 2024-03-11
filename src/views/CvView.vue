<script setup>
/* import CvPortfolio from '../components/CvPortfolio.vue'; */
</script>


<template>
<div class="Wrapping">
<div class="item3">
  <h3 id="Utbildning">Utbildning</h3>
      <div v-if="cv.Utbildning.length > 0">
        <div v-for="info in cv.Utbildning" :key="info.id">
          <div>
            <h5>{{ info.Titel }}</h5>
            <p>{{ info.Program }}</p>
            <p>{{ info.År }}</p>
          </div>
        </div>
      </div>
      <div v-else>Loading...</div>
    </div>

<div class="item4">
  <h3 id="Kompetenser">Kompetenser</h3>
      <div v-if="cv.Kompetenser.length > 0">
        <div v-for="info in cv.Kompetenser" :key="info.id">
          <div>
            <h5>{{ info.id }}</h5>
            <p>{{ info.Titel }}</p>
          </div>
        </div>
      </div>
      <div v-else>Loading...</div>
    </div>
<div class="item5">
  <h3 id="Arbete">Arbete</h3>
      <div v-if="cv.Arbete.length > 0">
        <div v-for="info in cv.Arbete" :key="info.id">
          <div>
            <h5>{{ info.Arbetsgivare }}</h5>
            <p>{{ info.Titel }}</p>
            <p>{{ info.Arbete }}</p>
            <p>{{ info.År }}</p>
          </div>
        </div>
      </div>
      <div v-else>Loading...</div>
    </div>
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

/* Grid Container */
.Wrapping {
  display: grid;
  height: 100vh;
  grid-template-columns: 1fr 1fr 1fr;
  grid-template-rows:

    0.8fr;

    grid-template-areas:
     "item3 item4 item5";
}

.item3{
  display: grid;
  grid-area: item3;
  justify-items: center;
  align-items: start;
  font-size: large;
  margin: 2rem;
  border: solid 0.2em #A0658D;
  background-color: #F0F0F0;
  color: #3d2636;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

#Utbildning{
  display: grid;
  margin: 1rem;
}

.item4{
  display: grid;
  grid-area: item4;
  justify-items: center;
  align-items: start;
  font-size: large;
  margin: 2rem;
  border: solid 0.2em #A0658D;
  background-color: #F0F0F0;
  color: #3d2636;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
 }

#Kompetenser{
  display: grid;
  margin: 1rem;
}

.item5{
  display: grid;
  grid-area: item5;
  justify-items:center;
  align-items: start;
  font-size: large;
  margin: 2rem;
  border: solid 0.2em #A0658D;
  background-color: #F0F0F0;
  color: #3d2636;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

#Arbete{
  display: grid;
  margin: 1rem;
}

p{
  display: grid;
  /* justify-items: start; */
  justify-content: start;
  /* justify-items: self-start; */
  width: 30vh;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}


/* @media (min-width: 900px)

{
  .wrapping{
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 1fr 1fr;
    grid-template-areas:
    "item3 item4 item5";
  }
}
 */
@media (max-width:500px) {

  .Wrapping {
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 0.5fr 0.2fr;
    grid-template-areas:
      "item3 item4 item5";

    display: inline;

    /* .item3{
      margin: 1rem;
    }

    .item4{
      margin: 1rem;
    }

    .item5{
      margin: 1rem;
    } */

  }

}
</style>
