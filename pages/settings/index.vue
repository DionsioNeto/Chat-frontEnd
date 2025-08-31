<script setup>
useHead({
  title: "Settings | TMJ",
  meta: [{
      name: "description",
      content: "some description"
      },
  ]
})



const open = ref(false)

function toggleDropdown() {
  open.value = !open.value
}

function closeDropdown() {
  open.value = false
}
</script>
<template>
  <div class="dark:text-neutral-300 flex gap-5 items-center border-2 border-neutral-700 p-3 rounded-xl sticky top-0 bg-neutral-950 z-30">
    <NuxtLink 
      class="bg-neutral-800 rounded-full border-2 border-neutral-700"
      to="/"
    >
      <IconChevronLeft :size="30"/>
    </NuxtLink>
    <h1 class="text-xl font-bold">Settings</h1>
  </div>

  <section class="">
    <ul>
      <li>
        <NuxtLink to="">
          <div class="flex items-center justify-between p-2">
            <div class="flex items-center gap-2">
              <IconUser/> 
              <span>Estado da conta</span>
            </div>
            <IconChevronRight/> 
          </div>
        </NuxtLink>
      </li>

    </ul>
  </section>    
    
</template>