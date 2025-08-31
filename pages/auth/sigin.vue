<script setup>
useHead({
    title: "Sigin | TMJ",
    meta: [{
        name: "description",
        content: "some description"
        },
    ]

})


definePageMeta({
  layout: "simple"
})

</script>

<template>
  <main class="flex flex-col items-center justify-center min-w-screen min-h-[90vh] py-6 gap-3">
    <Logo />
    <h1 class="text-2xl font-bold">Seja bem vindo (a)!</h1>
    <p class="text-neutral-600">
        Já tenho uma conta
        <NuxtLink 
            class="underline underline-offset-4 hover:text-neutral-700"
            to="/auth/login"
        >
        Iniciar sessão
        </NuxtLink>
    </p>
    <form action="" class="flex flex-col gap-4 min-w-80">
        <div class="flex flex-col gap-1">
            <input 
                class="w-full rounded-xl p-2 bg-neutral-950 border"
                type="text" 
                placeholder="Enter you email"
            >
        </div>

        <div class="flex flex-col gap-1">
            <input 
                class="w-full rounded-xl p-2 bg-neutral-950 border"
                type="text" 
                placeholder="Enter you Password"
            >
        </div>
        <NuxtLink 
            to="" 
            class="text-sm underline underline-offset-4 text-neutral-700 hover:text-neutral-600"
        >
            Esqueceu a sua palavra-passe?
        </NuxtLink>
        <button
            class="w-full rounded-xl p-2 bg-neutral-600" 
            type="submit"
        >
            Login
        </button>
    </form>
    <section class="">
        <div class="relative flex items-center justify-center text-gray-500">
            <span class="px-2 relative before:content-[''] before:block before:h-[1px] before:w-24 before:bg-gray-500 before:absolute before:top-1/2 before:-left-28 after:content-[''] after:block after:h-[1px] after:w-24 after:bg-gray-500 after:absolute after:top-1/2 after:-right-28">
                ou
            </span>
        </div>
    </section>
  </main>
  <FooterInfo/>
</template>