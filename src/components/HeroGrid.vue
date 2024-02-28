<script setup>
</script>


<template>
  <div id="wrapper-hero">

      <!-- <img
          src="../assets/img/annie-spratt-nWiS2rgtVts-unsplash.jpg"

      /> -->

      <div class="centered">
          <h1>Frida Häggström</h1>
          <h3>Frontend developer - student</h3>
      </div>

  </div>
</template>



<style>
   /* Stilar för att centrera och justera utseendet av hero-sektionen */
  /*  #wrapper-hero img { */
        /* margin: 0 auto; */    /* Centrerar bilden horisontellt */
        /* height: auto;  */     /* Gör bilden responsiv för olika skärmstorlekar */
        /* overflow-x: hidden; */ /* Döljer eventuell horisontell overflow av bilden */
    /*     background-image: cover;
    } */

    /* Stilar för centrerad text */
    #wrapper-hero .centered {
        position: absolute; /* Absolut positionering relativt till första föräldern med relativ eller absolut positionering */
        top: 50%;           /* Centrerar vertikalt till 50% av förälderns höjd */
        left: 50%;          /* Centrerar horisontellt till 50% av förälderns bredd */
        transform: translate(-50%, -50%); /* Justerar positionen så att centrum av elementet hamnar exakt i mitten */
        color: white;       /* Sätter textfärg till vit */
    }

</style>
