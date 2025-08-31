<script setup>
useHead({
  title: "Stories | TMJ",
  meta: [{
      name: "description",
      content: "some description"
      },
  ]
})
</script>
<template>
  <Bt>
    <template #path>
      <NuxtLink 
        class="bg-neutral-800 rounded-full border-2 border-neutral-700"
        to="/"
      >
        <IconChevronLeft :size="30"/>
      </NuxtLink>
    </template>
    <template #Title>
      Stories
    </template>
  </Bt>
       

    <section class="">
     

    </section>

        

</template>
