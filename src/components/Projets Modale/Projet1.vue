<template>
    <div class="bloc-modale" v-if="revele">
      <div class="overlay" v-on:click="toggleModale"></div>
  
      <div class="modale">
        <div v-on:click="toggleModale" class="btn-modale">X</div>
        <h1>Cv en HTML5 et CSS3</h1>
        <p>Date de création : <time datetime="2024-04-26">26 Avril 2024</time></p>
        <p>Technologies utilisées :</p>
        <ul>
          <li>HTML5</li>
          <li>CSS3</li>
          <li>Github</li>
        </ul>
        <p>Pour plus de détails <a href="https://github.com/kilianaBldr/CV-Kiliana.git" target="_blank">GitHub</a></p>
      </div>
    </div>
  </template>
  
  
  <script>
  export default {
    name: "Projet1",
    props: ["revele", "toggleModale"]
  };
  </script>
  
  
  <style scoped>
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
  
  .overlay {
    background: rgba(0, 0, 0, 0.5);
    position: fixed;
    top: 0;
    bottom: 0;
    left: 0;
    right: 0;
  }
  
  .modale {
    background: #f1f1f1;
    color: #333;
    padding: 50px;
    position: fixed;
    top: 30%;
  }
  
  .btn-modale {
    position: absolute;
    top: 10px;
    right: 10px;
  }
  </style>