<script setup>
</script>

 <template>
  <div class="container">
    <div class="Profile">
      <img src="../assets/img/billy-huynh-W8KTS-mhFUE-unsplash.jpg" alt="Profilpicture">
    </div>
    <div class="Presentation">
    <div >
      <h1>Frida Häggström</h1>
      <h3>Frontend developer - student</h3>
    </div>
    </div>
    </div>
</template>

<style>
/* Grid Container */
.container {
  display: grid;
  height: 100vh;
  grid-template-columns: 0.5fr 0.5fr;
  grid-template-rows:

    /* item1 */
    1fr
    /*item2*/
    1fr;

    grid-template-areas:

    "item1 item2"
    "item1 item2";
}

.Profile {
  grid-area: item1;
  display: grid;
  justify-items: center;
  align-items: center;

}

.Presentation {
  display: grid;
  grid-area: item2;
  justify-content:start;
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
    grid-template-rows: 0.6fr 0.6fr ;
    grid-template-areas:
      "item1"
      "item2";
      display: inline;
  }

  .Profile img{
    margin-top: 5vh;
    margin-bottom: 5vh;
    height: 300px;
    width: 300px;
  }

  h1,h3{
    margin-left:20%;
    margin-bottom: 2vh;

  }
}

</style>
