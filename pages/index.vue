<script setup>
useHead({
  title: "Home | TMJ",
  meta: [{
      name: "description",
      content: "some description"
      },
  ]
})

definePageMeta({
  layout: 'default'
})
</script>
<template>
  
    <div class="dark:text-neutral-300 flex gap-5 items-center border-2 border-neutral-700 p-3 rounded-xl sticky top-0 bg-neutral-950 z-30">
      <NuxtLink 
        class="bg-neutral-800 rounded-full border-2 border-neutral-700"
        to="/"
      >
        <IconChevronLeft :size="30"/>
      </NuxtLink>
      <h1 class="text-xl font-bold">Home</h1>
    </div>    
    <section class="">
home
    </section>
  
</template>