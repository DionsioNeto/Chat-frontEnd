<script setup lang="ts">
  import { ref } from 'vue';
  const toggleModal = ref(false)
  function nn(){
    toggleModal.value = !toggleModal.value
  }

  const showModal = ref(false)


</script>

<template>

  <aside class="fixed left-1 hidden sm:block dark:text-neutral-300">
    <nav class="flex flex-col justify-between min-h-screen p-4 overflow-y-auto" >
      <Logo/>
      <ul>
        <li>
          <NuxtLink 
            to="/" 
            active-class="bg-neutral-700/50"
            class="flex justify-center lg:justify-start gap-3 hover:dark:bg-neutral-700 hover:bg-neutral-300 p-2 rounded-xl items-center mb-1"
          >
            <IconHome :size="25"/> <span class="hidden lg:block font-bold">Home</span>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink
            to="/message" 
            active-class="bg-neutral-700/50"
            class="flex justify-center lg:justify-start gap-3 hover:dark:bg-neutral-700 hover:bg-neutral-300 p-2 rounded-xl items-center mb-1"
          >
            <IconMessageSquare :size="25"/> <span class="hidden lg:block font-bold">Message</span>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink 
            to="/notifications" 
            active-class="bg-neutral-700/50"
            class="flex justify-center lg:justify-start gap-3 hover:dark:bg-neutral-700 hover:bg-neutral-300 p-2 rounded-xl items-center mb-1"
          >
            <IconBell :size="25"/><span class="hidden lg:block font-bold">Notification</span>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink 
            to="/stories" 
            active-class="bg-neutral-700/50"
            class="flex justify-center lg:justify-start gap-3 hover:dark:bg-neutral-700 hover:bg-neutral-300 p-2 rounded-xl items-center mb-1"
          >
            <IconShapes :size="25"/><span class="hidden lg:block font-bold">Stories</span>
          </NuxtLink>
        </li>
                <li>
          <NuxtLink 
            to="/search" 
            active-class="bg-neutral-700/50"
            class="flex justify-center lg:justify-start gap-3 hover:dark:bg-neutral-700 hover:bg-neutral-300 p-2 rounded-xl items-center"
          >
            <IconSearch :size="25"/> <span class="hidden lg:block font-bold">search</span>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink 
            to="/settings" 
            active-class="bg-neutral-700/50"
            class="flex justify-center lg:justify-start gap-3 hover:dark:bg-neutral-700 hover:bg-neutral-300 p-2 rounded-xl items-center"
          >
            <IconSettings :size="25"/> <span class="hidden lg:block font-bold">settings</span>
          </NuxtLink>
        </li>
      </ul>
        

      <div>
        <NuxtLink 
          to="/profile" 
          active-class="bg-neutral-700/50"
          class="flex justify-center gap-3 hover:dark:bg-neutral-700 hover:bg-neutral-300 p-2 rounded-xl items-center"
        >
          <IconUser :size="25"/>
        </NuxtLink>
        <button @click="showModal = true" class="flex justify-center gap-3 hover:dark:bg-neutral-700 hover:bg-neutral-300 px-2 py-1 rounded-xl items-center text-red-600 font-semibold w-full">
          <IconLogOut :size="25" />
        </button>
      </div>
    </nav>
  </aside>


  <teleport to="body">
    <Modal :show="showModal" @close="showModal = false">
      <template #header>
        Log Out?
      </template>

      <template #body>
        <NuxtLink to="/auth/Login">
          Login
        </NuxtLink>
      </template>

      <template #footer>
        
      </template>
    </Modal>
  </teleport>
</template>