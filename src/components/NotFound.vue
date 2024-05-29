<template>
    <section class="error">
        <div class="errorTexte">
        <p>Oupss! Page introuvable !</p>
        <h1>Error 404</h1>
        <p>Voulez-vous retourner sur la page d'<router-link to="/">acceuil</router-link></p>
        </div>
        <div class="imageError">
            <img src="../assets/img/image-error.jpg" alt="image d'une personne a la fenetre">
        </div>
    </section>
</template>
<script setup>

</script>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Poetsen+One&display=swap');
@import url('https://fonts.googleapis.com/css2?family=Chakra+Petch:ital,wght@0,300;0,400;0,500;0,600;0,700;1,300;1,400;1,500;1,600;1,700&display=swap');
*{
    width: 100%;
}
section {
    display: flex;
    color: rgb(182,112,118);
    border-radius: 10px;
    padding: 30px;
    margin: 5px auto ;
    background-color: rgb(0,0,0);
}
.errorTexte {
    text-align: center;
    padding: 10px;
    padding-right: 50px;
}
h1 {
    font-family: "Poetsen One", sans-serif;
    font-size: xx-large;
}
p {
    font-family: "Chakra Petch", sans-serif;
    font-size: 20px;
}
.imageError {
    padding-left: 40px;
}
img {
    width: 467px;
    height: 600px;
}

</style>