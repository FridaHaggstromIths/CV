 import CvPortfolio from 
 
 
 
 <!-- rendera ut från fetch? -->

<template>
  <div>
    <h1>
      {{ CvPortfolio }}
    </h1>
    
 
  </div>
</template>

<script>

    export default {
        // Data-funktion som returnerar initiala data för komponenten
        data() {
            return {
                cv: []     // En tom lista 
                
            }
        },
        name: 'CvView',  // Namn på komponenten
        components: {'Cv-Portfolio': CvPortfolio },  // Användning av komponenten
        created() {
            // Efter att komponenten har monterats, hämta data från spa json-filen
            this.fetchData()
        },
        methods: {
            // En metod för att hämta spa-data från en json-fil asynkront
            async fetchData() {
                const res = await fetch('Kompetenser.json')
                const val = await res.json()
                this.cv = val  // Sätter data från filen till 'spas'-listan
            }
        }
      }
</script>