<template>
    <footer class="flex justify-center sm:pb-5 pb-12">
        <div class="text-xs  max-w-80 text-center">
            <span>&copy; TMJ {{ year }}</span> |
            <NuxtLink
                class="underline underline-offset-2 mx-2"
                to=""
            >
                Sobre
            </NuxtLink> |
            <NuxtLink
                class="underline underline-offset-2 mx-2"
                to=""
            >
                Blogue
            </NuxtLink> |
            <NuxtLink
                class="underline underline-offset-2 mx-2"
                to=""
            >
                Ajuda
            </NuxtLink> |
            <NuxtLink
                class="underline underline-offset-2 mx-2"
                to=""
            >
                Privacidade
            </NuxtLink> |
            <NuxtLink
                class="underline underline-offset-2 mx-2"
                to=""
            >
                Termos
            </NuxtLink> |
            <NuxtLink
                class="underline underline-offset-2 mx-2"
                to=""
            >
                Verificação
            </NuxtLink>
        </div>
    </footer>
</template>
<script setup>
    let year = new Date().getFullYear();
</script>