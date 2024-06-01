<template>
  <footer>
    <div>
      <a class="linkFooter" href="https://github.com/kilianaBldr"><img class="linkFooter" src="../assets/img/github.png"
          alt="Logo Github"></a>
      <a class="footer" href=""><img class="linkFooter" src="../assets/img/linkedin.png" alt="Logo Linkedin"></a>
    </div>
    <p><small>Dernière mise à jour le <time datetime="2024-05-27">27 Mai 2024</time> . </small></p>
  </footer>
</template>

<script setup>
</script>

<style>
footer {
  color: rgb(239 192 160 / 88%);
  padding: 15px;
  text-align: center;
}

.linkFooter {
  height: 40px;
  width: 40px;
  padding: 2px;
}

.linkFooter:hover {
  cursor: pointer;
  opacity: 0.3;
}
</style>