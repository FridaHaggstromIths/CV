<script setup>
import { RouterLink, RouterView } from 'vue-router'
</script>


<template>
  <header>
    <nav>
      <ul class="ul-navlink">
        <RouterLink class="navlink" to="/">Home</RouterLink>
        <RouterLink class="navlink" to="/CvView">CV</RouterLink>
      </ul>
    </nav>
  </header>
  <RouterView />
</template>


<style scoped>
nav {
  grid-area: nav;
  position: sticky;
  width: 100%;
  height: 10vh;
  background-color: #A0658D;
  font-size: 2em;
  font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif
}

.ul-navlink {
  position: absolute;
  bottom: 2%;
  margin-left: 70vw;
  top: 5%
}

.navlink {
  text-decoration: none;
  display: inline;
  color: #ffffff;
  list-style-type: none;
  margin: 5vh;
}

.navlink:hover {
  color: #3e0c3f;
}
</style>
