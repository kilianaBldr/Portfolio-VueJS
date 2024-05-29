<template>
    <header>
        <a href="#presentation"><img alt="Portfolio Logo" class="logo" src="../assets/img/logo.png"  /></a>

        <div class="wrapper">
            <nav>
                <a class="link" href="#presentation"> Qui suis-je ?</a>
                <a class="link" href="#projets">Mes Projets</a>
                <a class="link" href="#contact">Me Contacter</a>
            </nav>
        </div>
    </header>

    <RouterView />
</template>

<style scoped>
@import url('https://fonts.googleapis.com/css2?family=Rubik:ital,wght@0,300..900;1,300..900&display=swap');

* {
    box-sizing: border-box;
}

header {
    display: flex;
    justify-content: center;
    align-items: center;
    background-color: rgba(88, 52, 68, 0.596);
    position: sticky;
    width: 100%;
    left: 0;
    line-height: 1.5;
    max-height: 100vh;
}

.logo {
    width: 60px;
    margin-top: 10px;

}

nav {
    position: static;
    display: flex;
    align-items: center;
    font-family: "Rubik", sans-serif;
    font-optical-sizing: auto;
    justify-content: center;
    width: 100%;
    text-align: center;
    margin: 10px;

}

a {
    color: rgb(243, 189, 173);
    transition: 0.2s;
    padding: 3px;
}


nav a {
    display: inline-block;
    padding: 0 1rem;
    border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
    border: 0;
}
@media (hover: hover) {
  a:hover {
    background-color: hsla(288, 56%, 2%, 0.155);
    border-bottom: 1px solid black;
  }
}
</style>