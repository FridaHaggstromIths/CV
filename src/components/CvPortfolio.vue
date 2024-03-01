<!-- CvPortfolio.vue -->
<template>
  //

<!-- <div id="wrapping">
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
    </div> -->
  <!-- <div>
    <h1 class="headline">Cv</h1>
    <div v-for="utbildning in cv" :key="utbildning.id">
      <p>{{ utbildning.Titel }}</p>
      <p>{{ utbildning.Program }}</p>
      <p>{{ utbildning.År }}</p>
    </div>
  </div> -->
</template>

<script>
export default {
  props: {
    cv: {
      required: true,
      type: Array
    }
  }
}
</script>

<style scoped>


.headline {
        position: absolute; /* Absolut positionering relativt till första föräldern med relativ eller absolut positionering */
        top: 50%;           /* Centrerar vertikalt till 50% av förälderns höjd */
        left: 50%;          /* Centrerar horisontellt till 50% av förälderns bredd */
        transform: translate(-50%, -50%); /* Justerar positionen så att centrum av elementet hamnar exakt i mitten */
        color: #3d2636;       /* Sätter textfärg till vit */
        font-size:large;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    }

</style>
