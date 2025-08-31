<template>
  <div>
    <h1>Nuxt Lucide Icons</h1>
    <IconRocket />
    <IconFolderGit2 color="red" />
    <IconGithub :size="32" />
    <NuxtLink to="/">
        <IconHome/>
    </NuxtLink>
  </div>
</template>

<script setup>
useHead({
    title: "User | TMJ",
    meta: [{
        name: "description",
        content: "some description"
        },
    ]

})
</script>