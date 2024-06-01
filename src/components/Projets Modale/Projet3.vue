<template>
    <div class="bloc-modale" v-if="revele">
        <div class="overlay" v-on:click="toggleModale"></div>

        <div class="modale">
            <div v-on:click="toggleModale" class="btn-modale">X</div>
            <h1>Dynamiser un Espace Commentaire</h1>
            <p>Date de création : <time datetime="2024-05-23">23 Mai 2024</time></p>
            <div class="technologie">
                <h2>Technologies utilisées :</h2>
                <ul>
                    <li>HTML5</li>
                    <li>CSS3</li>
                    <li>JavaScript</li>
                    <li>Github</li>
                </ul>
            </div>
            <p>Pour plus de détails <a href="https://github.com/kilianaBldr/DynamiserUnEspaceCommentaire.git"
                    target="_blank">Github</a></p>
        </div>
    </div>
</template>


<script>
export default {
    name: "Projet3",
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
    background: #EEAAA5;
    color: #333;
    padding: 50px;
    position: fixed;
    top: 30%;
    border-radius: 5px;
}

.btn-modale {
    font-weight: bold;
    position: absolute;
    top: 10px;
    right: 15px;
}

h1 {
    margin-bottom: 15px;
    border-bottom: 1px solid black;
}

.technologie {
    margin: 10px;
}

h2 {
    font-size: 17px;
}

a:hover {
    border-bottom: 1px solid black;
}
</style>