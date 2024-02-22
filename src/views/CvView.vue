<script setup>
import HeroGrid from '../components/HeroGrid.vue';
</script>

<template>
<HeroGrid />
<div id="wrapping">
        <!-- En kolumn (col) med flexbox för att centrera innehållet -->
        <div class="col" v-if="portfolio">
            <!-- En kort (card) med bredd på 18 rem, som innehåller text -->
            <div class="card" style="width: 18rem">

                <!-- En kortkropp (card-body) med rendering -->
                <div class="card-body">
                    <!-- En rubrik (card-title) som visar rubriken och renderar ut utbildning? -->
                    <h5 class="card-title">{{ portfolio.Utbildning }}</h5>

                    <!-- En paragraf (p) som visar kompetenser och arbete -->
                    <p>{{ portfolio.Kompetenser }}</p>
                    <p>{{ portfolio.Arbete }}</p>


                </div>
            </div>
        </div>
        <div v-else>Loading...</div>
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
        components: {'Cv-portfolio': CvPortfolio },  // Användning av komponenten
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
