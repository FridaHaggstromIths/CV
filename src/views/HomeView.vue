<script setup>
/* import HeroGrid from "../components/HeroGrid.vue" */
/* import PictureComponent from "../components/PictureCompanent.vue" */
</script>

<template>


  <div class="centered">
          <h1>Frida Häggström</h1>
          <h3>Frontend developer - student</h3>
  </div>

  <div class="Profile">
    <img src="../assets/img/billy-huynh-W8KTS-mhFUE-unsplash.jpg" alt="Profilpicture">

  </div>

  <!-- <HeroGrid /> -->
  <!-- <PictureComponent /> -->
</template>


<style>


/* Stilar för centrerad text */
    .centered {
        position: absolute; /* Absolut positionering relativt till första föräldern med relativ eller absolut positionering */
        top: 50%;           /* Centrerar vertikalt till 50% av förälderns höjd */
        left: 50%;          /* Centrerar horisontellt till 50% av förälderns bredd */
        transform: translate(-50%, -50%); /* Justerar positionen så att centrum av elementet hamnar exakt i mitten */
        color: white;       /* Sätter textfärg till vit */
    }
    .Profile img{
      width: 500px;
      height: 500px;
      border-radius: 50%;
      grid-area: item1;
      margin-left: 5%;
      margin-top: 2%;


}
</style>
