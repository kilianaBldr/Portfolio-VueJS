<template>
    <header>
        <a href=""><img alt="Vue logo" class="logo" src=""  /></a>

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
    background-color: rgba(88, 52, 68, 0.596);
    position: fixed;
    width: 100%;
    left: 0;
    line-height: 1.5;
    max-height: 100vh;
}

.logo {
    width: 70px;
    
    display: flex;
    margin: 1rem auto 1rem;
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



nav a.router-link-exact-active {
    color: var(--color-text);
}

nav a.router-link-exact-active:hover {
    background-color: transparent;
}

nav a {
    display: inline-block;
    padding: 0 1rem;
    border-left: 1px solid var(--color-border);
}

nav a:first-of-type {
    border: 0;
}
</style>