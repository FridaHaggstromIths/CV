<template>
  <footer>

      <ul>
        <a class="footerlink" href="https://www.linkedin.com/in/frida-h%C3%A4ggstr%C3%B6m-a7a149105/">&copy; Frida
          Häggström LinkedIn Profile
        </a>
      </ul>

  </footer>
</template>


<style>
footer {
  display: grid;
  /* grid-area: footer; */
  height: 8vh;
  width: 100%;
  background-color: #A0658D;
  color: white;
  font-size: 1em;
  font-family: 'Lucida Sans', 'Lucida Sans Regular', 'Lucida Grande', 'Lucida Sans Unicode', Geneva, Verdana, sans-serif;
  font-weight: 400;
  /* margin-top: 20vh; */
}

 .footerlink {
  display: grid;
  color: #ffffff;
  list-style: none;
  justify-items: center;
  align-items:center;
  text-decoration: none;
  margin-top:2vh;

}

.footerlink:hover {
  color: #3e0c3f;
}
</style>
