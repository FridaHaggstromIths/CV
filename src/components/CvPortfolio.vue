<!-- CvPortfolio.vue -->
<template>
  <div>
    <h1 class="headline">Cv Portfolio </h1>
    <div v-for="utbildning in cv" :key="utbildning.id">
      <p>{{ utbildning.Titel }}</p>
      <p>{{ utbildning.Program }}</p>
      <p>{{ utbildning.År }}</p>
    </div>
  </div>
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

.headline{
  color: #3d2636;
  font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif
}

</style>
