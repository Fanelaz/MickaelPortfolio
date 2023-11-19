<template>
  <div class="bloc-modale">
    <div class="overlay" v-on:click="$emit('closeModale')"></div>

    <div class="modale card">
      <div v-on:click="$emit('closeModale')" class="btn-modale">X</div>
      <h2>{{ title }}</h2>
      <p class="date">Créé le {{ date_creation }}</p>
      <img :src="img_URL" alt="image" class="imgdesc" />
      <div class="projects">
        <a v-bind:href="github" target="_blank" class="github-button">
          Github
        </a>
      </div>
      <div class="lang">
        <div class="techno" v-for="techno in props.technologies" :key="techno">
          <span v-if="technoLogo[techno]">
            <img
              :src="technoLogo[techno]"
              :alt="`Logo ${techno}`"
              class="logo"
            />
          </span>
        </div>
      </div>
    </div>
  </div>
</template>

<script setup>
const props = defineProps([
  "title",
  "technologies",
  "img_URL",
  "date_creation",
  "github",
]);

const technoLogo = {
  html: "../img/html-5.png",
  css: "../img/css-3.png",
  javascript: "../img/javascript.png",
  vuejs: "../img/vuejs.png",
  pdf: "../img/pdf.png",
};
</script>

<style scoped>
.overlay {
  background: rgba(0, 0, 0, 0.5);
  position: absolute;
  top: 0;
  left: 0;
  height: 100%;
  width: 100%;
}

.logo {
  height: 50px;
}
.lang {
  display: flex;
  align-items: center;
  justify-content: center;
  column-gap: 20px;
}
.github-button {
  background-color: #333;
  border: none;
  color: white;
  padding: 10px 20px;
  text-decoration: none;
  display: flex;
  font-size: 20px;
  margin: 4px 2px;
  cursor: pointer;
  transition: background-color 0.3s;
  justify-content: center;
}

.github-button:hover {
  background-color: #444;
}

.imgdesc {
  height: 300px;
}
.bloc-modale {
  position: fixed;
  top: 0;
  bottom: 0;
  left: 0;
  right: 0;
  display: flex;
  justify-content: center;
  align-items: center;
}

.modale {
  background: #f1f1f1;
  color: #333;
  padding: 50px;
  position: absolute;
  top: 10%;
  font-family: cursive;
}

.btn-modale {
  position: relative;
  background: none;
  border: none;
  font-size: 24px;
  cursor: pointer;
  outline: none;
  color: #555;
  margin-left: auto;
  color: rgb(124, 0, 0);
  border-style: solid;
  border-radius: 100%;
  width: 35px;
  text-align: center;
}

.btn-modale:hover {
  color: rgb(255, 0, 0);
}
.date {
  display: flex;
  justify-content: end;
  align-items: end;
  text-decoration: underline;
}
</style>
