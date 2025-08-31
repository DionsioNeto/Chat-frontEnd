<script setup>
  useHead({
    title: "Message | TMJ",
    meta: [{
        name: "description",
        content: "some description"
      },
    ]
  });

  const open = ref(false)

  function toggleDropdown() {
    open.value = !open.value
  }

  function closeDropdown() {
    open.value = false
  }

  const msg = ref("");



definePageMeta({
  layout: false
})

</script>
<template>
  <Sidbar/>
  <main class="flex flex-col h-screen sm:pl-28 sm:pr-44 lg:pl-44 sm:pt-6 p-3 pb-10 sm:pb-0">
    <!-- HEADER -->
    <div class="dark:text-neutral-300 flex gap-5 items-center p-1 rounded-xl sticky top-0 bg-neutral-950 z-30">
      <div class="flex gap-3 my-2 w-full">
        <NuxtLink 
          class="bg-neutral-800 rounded-full border-2 border-neutral-700 flex justify-center items-center"
          to="/message"
        >
          <IconChevronLeft :size="30"/>
        </NuxtLink>

        <div class="relative rounded-full overflow-hidden min-w-14 min-h-14 -z-2">
          <img 
            class="w-full h-full absolute"
            src="~/assets/img/avatar.jpg" 
            alt="Dionísio Neto"
          >
        </div>

        <div class="w-full">
          <div class="flex justify-between items-center">
            <div class="text-xl font-bold">Dionísio Neto
              <IconBadgeCheck class="inline text-blue-500" :size="18"/>
            </div>
            <div class="relative inline-block text-left">
              <!-- Botão -->
              <button @click="toggleDropdown">
                <div class="hover:bg-neutral-800 p-1 rounded-lg">
                  <IconCircleEllipsis/>
                </div>
              </button>

              <!-- Dropdown -->
              <transition
                enter-active-class="transition ease-out duration-200"
                enter-from-class="opacity-0 translate-y-1"
                enter-to-class="opacity-100 translate-y-0"
                leave-active-class="transition ease-in duration-150"
                leave-from-class="opacity-100 translate-y-0"
                leave-to-class="opacity-0 translate-y-1"
              >
                <div
                  v-if="open"
                  class="absolute right-0 mt-1 w-44 origin-top-right rounded-lg bg-neutral-800 shadow-lg ring-1 ring-black ring-opacity-5 focus:outline-none"
                >
                  <div class="py-2">
                    <NuxtLink
                      to="/profile"
                      class="block p-2 text-sm text-white hover:bg-neutral-900/50 transition font-bold"
                      @click="closeDropdown"
                    >
                      <IconUserSearch class="inline"/> See profile
                    </NuxtLink>
                    <NuxtLink
                      to="/settings"
                      class="block p-2 text-sm text-white hover:bg-neutral-900/50 transition font-bold"
                      @click="closeDropdown"
                    >
                      <IconSettings2 class="inline"/>
                      Configurações
                    </NuxtLink>
                    <button
                      class="text-start w-full block p-2 text-sm hover:bg-neutral-900/50 transition font-bold text-red-600"
                      @click="closeDropdown"
                    >
                      <IconUserLock class="inline"/> Black user
                    </button>
                  </div>
                </div>
              </transition>
            </div>
          </div>

          <div class="flex items-center justify-between">
            <div class="text-sm flex text-green-600 font-semibold">Online</div>
          </div>  
        </div>
      </div>
    </div>    

    <!-- CHAT COM SCROLL -->
    <section class="flex-1 overflow-y-auto py-3">
      <div class="w-full text-xs text-start ">12:10 h | 27/08/2025</div>
      <div class="my-2 flex justify-start">
        <div class="bg-neutral-200 text-black w-fit max-w-[60%] h-auto py-1 px-2 rounded-2xl">Boa noite</div>
      </div>

      <div class="w-full text-xs text-end ">12:11 h | 27/08/2025</div>
      <div class="my-2 flex justify-end">
        <div class="bg-neutral-900 text-white w-fit max-w-[60%] h-auto py-1 px-2 rounded-2xl">Boa noite, como vai tudo?</div>
      </div> 

      <div class="w-full text-xs text-end ">12:11 h | 27/08/2025</div>
      <div class="my-2 flex justify-end">
        <div class="bg-neutral-900 text-white w-fit max-w-[60%] h-auto py-1 px-2 rounded-2xl">Boa noite, como vai tudo?</div>
      </div>      

      <div class="w-full text-xs text-end ">12:11 h | 27/08/2025</div>
      <div class="my-2 flex justify-end">
        <div class="bg-neutral-900 text-white w-fit max-w-[60%] h-auto py-1 px-2 rounded-2xl">Boa noite, como vai tudo?</div>
      </div> 

      <div class="w-full text-xs text-end ">12:11 h | 27/08/2025</div>
      <div class="my-2 flex justify-end">
        <div class="bg-neutral-900 text-white w-fit max-w-[60%] h-auto py-1 px-2 rounded-2xl">Boa noite, como vai tudo?</div>
      </div> 

      <div class="w-full text-xs text-end ">12:11 h | 27/08/2025</div>
      <div class="my-2 flex justify-end">
        <div class="bg-neutral-900 text-white w-fit max-w-[60%] h-auto py-1 px-2 rounded-2xl">Boa noite, como vai tudo?</div>
      </div> 

      <div class="w-full text-xs text-end ">12:11 h | 27/08/2025</div>
      <div class="my-2 flex justify-end">
        <div class="bg-neutral-900 text-white w-fit max-w-[60%] h-auto py-1 px-2 rounded-2xl">Boa noite, como vai tudo?</div>
      </div> 
    </section>
    
    <!-- FORM FIXO EM BAIXO -->
    <section class="p-1">
      <form 
        action="" 
        method="post" 
        class="flex justify-between items-center gap-1 p-1 rounded-xl bg-neutral-300 dark:bg-neutral-900"
      >
        <div class="rounded-full bg-neutral-300 dark:bg-neutral-900 p-1">
          <IconCamera/>
        </div>

        <textarea 
          v-model="msg" 
          placeholder="Escreva..." 
          class="w-full rounded-lg p-1 min-h-10 outline-none resize-none bg-neutral-950"
        ></textarea>

        <div class="rounded-full bg-neutral-300 dark:bg-neutral-900 p-1" v-if="msg">
          <IconSendHorizonal/>
        </div>
        <div class="rounded-full bg-neutral-300 dark:bg-neutral-900 p-1" v-else>
          <IconMic/>
        </div>
      </form>
    </section>
  </main>
  <Aside/>
  <MobileNav/>
</template>