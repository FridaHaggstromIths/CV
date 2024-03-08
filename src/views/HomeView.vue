<!-- <script setup>
</script>


<template>
  <div class="Presentation">
          <h1>Frida Häggström</h1>
          <h3>Frontend developer - student</h3>
  </div>

  <div class="Profile">
    <img src="../assets/img/billy-huynh-W8KTS-mhFUE-unsplash.jpg" alt="Profilpicture">
  </div>
</template>


<style>
    .Presentation {

      grid-area: item3;
        /* position: absolute; */
        /* top: 50%;
        left: 60%; */
        color: #3d2636;
        font-size:large;
        font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
    }
    .Profile img{
      grid-area: item1;
      width: 400px;
      height: 400px;
      border-radius: 50%;
      /* margin-left: 20vw;
      margin-top: 12vh; */
    }

</style>
 -->

 <script setup>
</script>

 <template>
  <div class="container">
    <div class="Profile">
      <img src="../assets/img/billy-huynh-W8KTS-mhFUE-unsplash.jpg" alt="Profilpicture">
    </div>
    <div class="Presentation">
      <h1>Frida Häggström</h1>
      <h3>Frontend developer - student</h3>
    </div>
  </div>
</template>

<style>
/* Grid Container */
.container {
  display: grid;
  height: 100vh;
  grid-template-columns: 1fr 1fr;
  grid-template-rows:

    /* NAV */
    /* 1fr */
    /* item1 */
    1fr
    /*item2*/
    1fr;
    /* FOOTER */
    /* 1fr; */

    grid-template-areas:
    /* "nav nav" */
    "item1 item2"
    "item1 item2";
    /* "footer"; */

}

.Profile {
  grid-area: item1;
  display: grid;
  justify-items: center;
  align-items: center;
}

.Presentation {
  grid-area: item2;
  display: grid;
  justify-items: center;
  align-items:center;
  color: #3d2636;
  font-size: large;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
}

.Profile img {
  width: 350px;
  height: 350px;
  border-radius: 50%;
}


@media (max-width:500px) {
  .container {
    grid-template-columns: 1fr;
    grid-template-rows: 1fr 0.5fr ;
    grid-template-areas:
      "item1"
      "item2";
  }
}
/*--------------------------*/
</style>
