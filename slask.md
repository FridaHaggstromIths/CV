SLASK KOD

----Main css----
body {
  margin: 0;
  padding: 0;
  min-width: 100vh;
  box-sizing: border-box;
  overflow-x: hidden;
  overflow-y: scroll;
  background-image: url(img/annie-spratt-nWiS2rgtVts-unsplash.jpg);
  background-size: cover
}


/* Grid Container */
.container {
  display: grid;
  height: 100vh;
  grid-template-columns: 1fr 1fr;
  grid-template-rows:

    /* NAV */
    1fr
    /* item1 item2 */
    1fr
    /*item1 item2*/
    1fr
    /* FOOTER */
    1fr;

  grid-template-areas:
    'nav nav'
    'item1 item2'
    'item1 item2  '
    'footer footer';
}

/*------------slut på main css--------------*/
