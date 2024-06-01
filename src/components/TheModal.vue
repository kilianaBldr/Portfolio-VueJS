<template>
    <div id="projets">
            <h1>Projets Réaliser</h1>
        <div class="elementProjet">
            <section>
                <div class="container">
                    <h2>CV</h2>
                    <img src="../assets/img/CV-HTML-CSS.png" alt="Image d'un Cv en HTML et CSS">
                    <Projet1 v-if="revele && currentProject === 1" :revele="revele" :toggleModale="toggleModale">
                    </Projet1>
                    <div v-on:click="() => toggleModale(1)" class="btn">Ouvrir</div>
                </div>
            </section>
            <section>
                <div class="container">
                    <h2>Cahier des Charges</h2>
                    <img src="../assets/img/Cahier-des-charges-.jpg" alt="Image d'une couverture d'un Cahier des chages">
                    <Projet2 v-if="revele && currentProject === 2" :revele="revele" :toggleModale="toggleModale">
                    </Projet2>
                    <div v-on:click="() => toggleModale(2)" class="btn">Ouvrir</div>
                </div>
            </section>
            <section>
                <div class="container">
                    <h2>Un Espace Commentaire</h2>
                    <img src="../assets/img/Dynamiser-un-espace-commentaire.png"
                        alt="Image D'un espace commentaire dynamique">
                    <Projet3 v-if="revele && currentProject === 3" :revele="revele" :toggleModale="toggleModale">
                    </Projet3>
                    <div v-on:click="() => toggleModale(3)" class="btn">Ouvrir</div>
                </div>
            </section>
        </div>
    </div>

</template>

<script>
import Projet1 from './Projets Modale/Projet1.vue';
import Projet2 from './Projets Modale/Projet2.vue';
import Projet3 from './Projets Modale/Projet3.vue';

export default {
    name: "PageModale",
    data() {
        return {
            revele: false
        };
    },
    components: {
        Projet1,
        Projet2,
        Projet3
    },
    methods: {
        toggleModale(projectNumber) {
            this.currentProject = projectNumber;
            this.revele = !this.revele;
        }
    }
};
</script>


<style scoped>
.container {
    border: 2px solid black;
    border-radius: 10px;
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: space-between;
    margin: 50px;
    margin-top: 30px;
    padding: 10px;
}

.container:hover {
    box-shadow: 15px 10px 11px 0px #333;
}

#projets {
    box-sizing: border-box;
    border-radius: 5% 5% 5% 5%;
    display: flex;
    flex-direction: column;
    align-items: center;


}

.elementProjet {
    display: flex;
    color: black;
}

img {
    border: 1px solid black;
    height: 315px;
    width: 245px;
}

.btn {
    margin-top: 15px;
    padding: 5px;
    border-radius: 15% 15% 15% 15%;
    border: 2px solid rgb(22, 21, 22);
}

.btn:hover {
    background-color: rgba(14, 13, 14, 0.407);
    border: 2px solid rgb(9, 9, 9);
    cursor: pointer;
}

h1 {
    color: black;
    margin-top: 80px;
}

h2 {
    font-size: 20px;
    text-align: center;
}
</style>