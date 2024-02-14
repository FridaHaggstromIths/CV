

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
