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
  display: flex;
  align-items: center;
  justify-content:end;
  /* position: sticky; */
  width: 100%;
  height: 8vh;
  background-color: #A0658D;
  font-size: 2em;
  font-family:'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif
}


.ul-navlink {
  display: flex;
  justify-items: end;
  /* justify-content:space-around; */
  /* align-items:end; */
  /* justify-items: end; */
  /* position: absolute; */
  /* bottom: 2%; */
  /* margin-left: 70vw; */
  /* top: 5% */
}

.navlink {
  display: flex;
  margin-left: 3vh;
  margin-right: 3vh;
  text-decoration: none;
  display: inline;
  color: #ffffff;
  list-style-type: none;
  /* margin: 5vh; */

}

.navlink:hover {
  color: #3e0c3f;
}
</style>
