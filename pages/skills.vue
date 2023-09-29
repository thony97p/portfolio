<template>
    <main class="skills">
        <h2>Ce que je sais faire</h2>
        <h3>Hard Skills</h3>
        <ul>
            <li>Front-end</li>
            <li>HTML</li>
            <li>CSS</li>
            <li>Sass (CSS)</li>
            <li>JavaScript</li>
            <li>Git & GitHub</li>
            <li>Vue.js</li>
            <li>API</li>
            <li>Base de données</li>
            <li>MongoDB</li>
        </ul>

        <h3>Soft Skills</h3>
        <ul>
            <li>Travail en équipe</li>
            <li>Sens de l'écoute</li>
            <li>Sens du détail</li>
            <li>Capable de m'adapter</li>
        </ul>

        <h3>Langues</h3>
        <ul class="column">
            <li>Français : Langue maternelle</li>
            <li>Créole de la Martinique : Langue maternelle</li>
            <li>Anglais : Niveau avancé</li>
            <li>Italien : Niveau intermédiaire</li>
        </ul>
    </main>
</template>

<style scoped lang="scss">
main {
    background-color: var(--dark-blue);

    h3 {
        margin-inline-start: 1.5em;
    }

    ul {
        margin-inline-start: 1.5em;
        display: flex;
        flex-wrap: wrap;
        gap: .75em
    }

    li {
        list-style: none;
        padding: .2em .6em;
        font-weight: 500;
        color: var(--lighter-blue);
        background-color: var(--darker-blue);
        border-radius: 20px;
        cursor: default;
    }
}
</style>