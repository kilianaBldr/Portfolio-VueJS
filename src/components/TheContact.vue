<template>
    <div id="contact">
        <h1>Me Contacter</h1>
        <section>
            <form ref="form" @submit.prevent="sendEmail">
                <label for="nom">Nom :</label>
                <input type="text" name="nom" v-model="nom" placeholder="Nom">
                <span v-if="errors.nom" class="error">{{ errors.nom }}</span>

                <label for="prenom">Prénom</label>
                <input type="text" name="prenom" v-model="prenom" placeholder="Prénom">
                <span v-if="errors.prenom" class="error">{{ errors.prenom }}</span>

                <label for="object">Object :</label>
                <input type="text" name="object" v-model="object" placeholder="Object">
                <span v-if="errors.object" class="error">{{ errors.object }}</span>

                <label for="message">Message :</label>
                <textarea name="message" v-model="message" placeholder="Message..."></textarea>
                <span v-if="errors.message" class="error">{{ errors.message }}</span>

                <button type="submit" value="Send">Envoyer</button>
            </form>
        </section>
    </div>
</template>

<script>
import emailjs from '@emailjs/browser'

export default {
    name: 'PartieContact',
    data() {
        return {
            nom: '',
            prenom: '',
            object: '', // Assurez-vous que ce nom correspond à celui utilisé dans le template
            message: '',
            errors: {}
        }
    },
    methods: {
        validateForm() {
            this.errors = {};

            if (!this.nom) {
                this.errors.nom = "Le nom est requis.";
            }
            if (!this.prenom) {
                this.errors.prenom = "Le prénom est requis.";
            }
            if (!this.object) {
                this.errors.object = "L'objet est requis.";
            }
            if (!this.message) {
                this.errors.message = "Le message est requis.";
            }

            return Object.keys(this.errors).length === 0;
        },
        sendEmail() {
            if (this.validateForm()) {
                const templateParams = {
                    to_name: 'Kiliana Blondron',
                    from_nom: this.nom,
                    from_prenom: this.prenom,
                    object: this.object,
                    message: this.message,
                }
                emailjs
                    .sendForm('service_k9gpdqk', 'template_biy5fxm', templateParams, this.$refs.form, {
                        from_nom: '',
                        from_prenom: '',
                        object: '',
                        message: '',
                    }).then(() => {
                        console.log('Envoyer avec Success !');
                        //reset form 
                        form.reset();
                    },
                        (error) => {
                            console.log('Erreur !!');
                        },
                    );
            }
        },
    },
};
</script>

<style>
* {
    box-sizing: border-box;
}

.contact {
    margin-top: 80px;
}

h1 {
    color: black;
    text-align: center;
    padding-bottom: 8px;
    border-bottom: 1px solid black
}

form {
    background-color: rgb(204, 132, 138);
    display: block;
    margin: auto;
    margin-top: 20px;
    text-align: center;
    width: 70%;
    padding: 20px;
    border-radius: 5px;
}

label {
    float: left;
}

input {

    box-sizing: border-box;
    width: 100%;
    padding: 10px;
    margin-top: 6px;
    margin-bottom: 16px;
    border: 1px solid black;
    border-radius: 4px;

}

textarea {
    width: 100%;
    height: 60px;
    padding: 10px;
    margin-top: 6px;
    margin-bottom: 16px;
    border: 1px solid black;
    border-radius: 4px;
}

button {
    justify-content: center;
    width: 15%;
    background-color: rgb(182, 112, 118);
    color: white;
    padding: 12px 20px;
    border: none;
    border-radius: 4px;
    cursor: pointer
}

button:hover {
    background-color: rgba(5, 5, 5, 0.401);
}

.error {
    color: red;
    font-size: 0.9em;
    margin-top: -10px;
    margin-bottom: 10px;
    display: block;
}
</style>
