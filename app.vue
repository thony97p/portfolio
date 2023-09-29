<template>
    <NuxtLayout>
        <NuxtPage />
    </NuxtLayout>
</template>

<style>
.page-enter-active,
.page-leave-active {
    transition: all 0.6s linear;
}

.page-enter-from,
.page-leave-to {
    transform: scale(0.95);
    filter: brightness(30%)
}
</style>