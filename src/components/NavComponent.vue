<!-- <template>
  <header>
    <nav class="navbar navbar-expand-lg bg-body-tertiary">
      <div class="container-fluid">
        <a class="navbar-brand" href="#">Frida </a>
        <button class="navbar-toggler" type="button" data-bs-toggle="collapse" data-bs-target="#navbarNav"
          aria-controls="navbarNav" aria-expanded="false" aria-label="Toggle navigation">
          <span class="navbar-toggler-icon"></span>
        </button>
        <div class="collapse navbar-collapse" id="navbarNav">
          <ul class="navbar-nav">
            <li class="nav-item">
              <a class="nav-link active" aria-current="page" href="#">Home</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">CV</a>
            </li>
            <li class="nav-item">
              <a class="nav-link" href="#">Ta bort?</a>
            </li>
            <li class="nav-item">
              <a class="nav-link disabled" aria-disabled="true">Ta bort?</a>
            </li>
          </ul>
        </div>
      </div>
    </nav>
  </header>
</template> -->


<!---NAVBAR-->
<template>
  <header>
    <nav>
      <ul class="ul-navlink">
        <li class="navlink"><a href="#">CV</a></li>
        <li class="navlink"><a href="#">Contact</a></li>
      </ul>
    </nav>
  </header>
</template>

<style scoped>
/* NAV M. LÄNKAR*/
nav {
  grid-area: nav;
  position: sticky;

  width: 100%;
  background-image: linear-gradient(#A0658D, rgba(0, 0, 0, 0));
  font-size: 2em;
  margin: 0%;
  padding-bottom: 5%;
  font-family: 'Times New Roman', Times, serif;
}

.ul-navlink {
  position: absolute;
  bottom: 2%;
  margin-left: 70vw;
  top: 5%
}

a,
.navlink {
  text-decoration: none;
  display: inline;
  color: #ffffff;
  list-style-type: none;
  margin: 1vh;
}

li a:hover {
  color: #000000;
}

/*--------------------------*/
</style>

<!--
<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
}



/* Style "loggan" */
.navbar-brand {
  color: white;
  font-weight: bold;

}

/* bakgrund navbar */
.container-fluid {
  background-color: #D2959C;
}

.navbar.navbar-expand-lg.bg-body-tertiary {
  background-color: #D2959C;
}


/* Stilar för navbar-toggler, sätter bakgrundsfärg till vit */
.navbar-toggler {
  background-color: white;
}
</style> -->
