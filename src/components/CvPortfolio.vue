<!-- CvPortfolio.vue -->
<template>
  <div>
    <h1>Cv Portfolio </h1>
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
