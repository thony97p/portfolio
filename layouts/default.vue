<script setup lang="ts">
const route = useRoute()
const id = computed(() => Number(route.params.id || 1) + 1) 
</script>

<template>
    <div>
        <header>
            <h2>Mon portfolio</h2>
            <nav>
                <NuxtLink to="/" :id="id">Présentation</NuxtLink>
                <NuxtLink to="/crafts" :id="id">Réalisations</NuxtLink>
                <NuxtLink to="/parcours" :id="id">Parcours</NuxtLink>
                <NuxtLink to="/skills" :id="id">Compétences</NuxtLink>
                <NuxtLink to="/contact">Contact</NuxtLink>
                <a href="" target="_blank">Mon CV</a>
            </nav>
        </header>
        <slot />

        <footer>
            <div>
                <a href="mailto:thony.william@live.fr">
                    <i class="fa-solid fa-envelope"></i>
                </a>
                <a href="https://codepen.io/thony97" target="_blank">
                    <i class="fa-brands fa-codepen"></i>
                </a>
                <a href="https://www.linkedin.com/in/anthony-william-jj10/" target="_blank">
                    <i class="fa-brands fa-linkedin"></i>
                </a>
            </div>
            <div><img src="/img/icon-green.png" alt="Logo Nuxt.js"></div>
            <div>&copy; 2023. Made with Nuxt.js, the intuitive framework.</div>
        </footer>
    </div>
</template>

<style scoped lang="scss">
header {
    position: sticky;
    z-index: 20;
    top: 0;
    min-height: 5em;
    background-color: var(--lighter-blue);

    display: flex;
    justify-content: space-between;
    align-items: center;

    h2 {
        margin: 0 1em;
        font-size: 2.25rem;
        color: var(--fake-black);
        line-height: 3;
    }

    nav {
        margin-inline-end: 1.5em;
        text-transform: uppercase;

        a {
            position: relative;
            display: inline-block;
            margin: .4em 0;
            padding: 0 .8em;
            color: var(--fake-black);
            text-decoration: none;
            font-size: small;
            font-weight: 500;
            letter-spacing: .075em;
            transition: color .2s ease-in-out;

            &:not(:first-child) {
                border-left: 1px solid var(--fake-black);
            }

            &:hover {
                color: var(--dark-blue);
            }

            &.router-link-exact-active {
                font-weight: 700;
            }
        }
    }
}

footer {
    min-height: 180px;
    background-color: var(--darker-blue);
    display: flex;
    flex-direction: column;
    gap: 5px;
    justify-content: center;
    color: var(--light-blue);

    div {
        display: flex;
        justify-content: center;
        align-items: center;
        gap: 1em;
    }

    img {
        height: 60px;
        width: auto;
        filter: saturate(90%)
    }

    a {
        display: inline-block;
        padding: .4em;
        font-size: 1.75rem;
        color: inherit;
        text-decoration: none;
        text-align: center;
        border-radius: 50%;
        transition: all .2s ease-in-out;

        &:hover {
            background-color: var(--light-blue);
            color: white !important;

            &:visited {
                color: inherit;
            }
        }
    }
}
</style>