<template>
    <main class="hello">
        <article id="me">
            <div class="square one"></div>
            <div class="square two"></div>
            <h2>Faisons connaissance...</h2>
            <p>Je m'appelle <strong>Anthony William</strong>, j'ai <strong>26 ans</strong> et je suis à la
                recherche d'une alternance en <strong>développement web full-stack</strong>.</p>
        </article>
        <article id="more">
            <p>J'ai commencé à apprendre le développement web seul en février-mars 2022. C'est un domaine tout
                nouveau pour moi et qui me plaît. J'aimerais développer mes connaissances et compétences et
                exercer ce métier de manière durable.
            </p>
            <p>Motivé à apprendre, toujours , j. Je suis inscrit à la <strong>3W Academy</strong> en parcours
                <strong>Full Stack Developer pour une durée de 12 mois</strong> en alternance.
            </p>
            <p>Ce portfolio a pour but de vous montrer plus en détails mes compétences au travers : de sa
                conception, et de mes autres réalisations. N'hésitez pas à <NuxtLink to="/contact">me contacter</NuxtLink>
                pour me donner votre feedback, pour plus de questions ou pour un entretien ;).</p>
            <div class="wrapper">
                <img src="/img/html-5.png" alt="Logo HTML 5" title="HTML 5">
                <img src="/img/css-3.png" alt="Logo CSS3" title="CSS 3">
                <img src="/img/js.png" alt="Logo JavaScript" title="JavaScript">
                <img src="/img/sass.png" alt="Logo Sass" title="Sass (Préprocesseur CSS)">
                <img src="/img/vue.png" alt="Logo du framework Vue.js" title="Vue.js, le framework JS évolutif">
                <img src="/img/github-logo.png" alt="Logo GitHub" title="L'outil GitHub">
            </div>
        </article>
    </main>
</template>

<style>
@import url("~/assets/css/style.css");

main {
    padding: 2.5em;
}
</style>

<style scoped lang="scss">
main {
    background-color: var(--light-blue);

    a {
        color: inherit;
    }

    #me {
        position: relative;
        height: 300px;
        width: 300px;
        margin-block-end: 2.5em;
        margin-inline: auto;
        padding: 3.5em;
        color: var(--whity);
        border: 3px solid var(--whity);

        display: flex;
        flex-direction: column;
        justify-content: space-between;

        h2 {
            font-size: 2em;
            font-weight: 600;
            text-align: center;
        }

        p {
            margin: 0;
            font-size: medium;
            text-align: justify;
        }

        .square {
            position: absolute;
            height: inherit;
            width: inherit;
            border: 2px solid var(--whity);
            transform-origin: center;


            &.one {
                top: -12px;
                left: -12px;
                padding: calc(3.5em + 10px);
                animation: spin-one 10s linear infinite, end 2s 20s linear forwards;
                animation-iteration-count: 2, 1;
            }

            &.two {
                top: -20px;
                left: -20px;
                padding: calc(3.5em + 18px);
                clip-path: polygon(0 0, 31% 0, 100% 83%, 100% 100%, 54% 100%, 0 15%);
                animation: breathe 4s linear infinite forwards;
            }
        }
    }

    #more {
        margin: 0 auto;
        max-width: 90%;
        color: var(--fake-black);
        font-weight: 500;
        text-align: justify;
    }

    .wrapper {
        text-align: center;

        img {
            margin: 1%;
            height: 50px;
            width: auto;
            filter: saturate(5%);
            transition: all .5s ease-out;
            transition-delay: .1s;

            &:hover {
                filter: saturate(100%);
            }
        }
    }
}

@keyframes spin-one {
    0% {
        opacity: 0;
        transform: rotate(0deg) scale(1);
    }

    5% {
        opacity: 1;
    }

    15% {
        transform: rotate(0deg) scale(1);
    }

    25% {
        transform: rotate(360deg);
        animation-timing-function: ease;
    }

    35%,
    75% {
        transform: rotate(720deg) scale(.8);
        opacity: 1;
    }

    90% {
        transform: rotate(0) scale(3);
        opacity: 0;
    }

    40% {
        animation-timing-function: linear;
    }

    100% {
        opacity: 0;
    }
}

@keyframes breathe {

    0%,
    100% {
        transform: scale(0.98);
    }

    50% {
        transform: scale(1.01);
    }

}

@keyframes end {
    0% {
        opacity: 0;
    }

    100% {
        opacity: 1;
        transform: scale(.8);
    }
}
</style>