<script setup>
</script>


<template>
  <div class="centered">
          <h1>Frida Häggström</h1>
          <h3>Frontend developer - student</h3>
  </div>

  <div class="Profile">
    <img src="../assets/img/billy-huynh-W8KTS-mhFUE-unsplash.jpg" alt="Profilpicture">

  </div>
</template>


<style>


/* Stilar för centrerad text */
    .centered {
        position: absolute; /* Absolut positionering relativt till första föräldern med relativ eller absolut positionering */
        top: 50%;           /* Centrerar vertikalt till 50% av förälderns höjd */
        left: 60%;          /* Centrerar horisontellt till 50% av förälderns bredd */
        transform: translate(-50%, -50%); /* Justerar positionen så att centrum av elementet hamnar exakt i mitten */
        color: #3d2636;       /* Sätter textfärg till vit */
        font-size:large;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    }
    .Profile img{
      width: 400px;
      height: 400px;
      border-radius: 50%;
      grid-area: item1;
      margin-left: 20vw;
      margin-top: 12vh;
    }

/* h1{
  background-image: url(img/annie-spratt-nWiS2rgtVts-unsplash.jpg);
  background-size: cover;
  background-clip: text;

} */
</style>
