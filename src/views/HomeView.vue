<template>
  <body>
    <div class="desc">
      <div id="name" class="name">
        <h1>LE BRETON<br />Mickaël</h1>
        <p id="presentation">
          Je suis un jeune développeur en pleine formation depuis le 05
          septembre 2023 <br />
          Je suis très motivé dans les projets qui touchent le monde de la
          programmation, depuis l'âge de mes 10 ans je souhaite en faire mon
          métier !!
        </p>

        <img
          class="img-logo"
          src="../assets/imgs/icons8-html-48.png"
          alt="logo HTML"
        />
        <img
          class="img-logo"
          src="../assets/imgs/icons8-css-48.png"
          alt="logo CSS"
        />
        <img
          class="img-logo"
          src="../assets/imgs/icons8-javascript-48.png"
          alt="logo JAVASCRIPT"
        />
      </div>
    </div>
  </body>
</template>

<script>
export default {
  name: "Accueil",
};
</script>

<style scoped>
body {
  width: auto;
  height: 1080px;
}

.desc {
  width: 100%;
}

#name {
  text-align: center;
  display: block;
  width: 100%;
  padding-top: 200px;
  margin-left: auto;
  margin-right: auto;
}

#name h1 {
  font-size: 3em; /* Ajustez la taille du texte selon vos besoins */
  color: rgb(255, 194, 80); /* Couleur du texte */
  font-family: "Roboto Mono", monospace;
  text-decoration: underline;
}

#name h1:hover {
  text-shadow: #fc0 1px 0 10px;
}

.img-logo {
  width: 100px;
  padding-left: 30px;
}

#presentation {
  font-size: 24px;
  color: black;
  width: 100%;
  margin-left: auto;
  margin-right: auto;

}

#presentation:hover {
  text-shadow: black 1px 0 10px;
}
</style>
