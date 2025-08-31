<script setup>
useHead({
  title: "Message | TMJ",
  meta: [{
      name: "description",
      content: "some description"
      },
  ]
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
      <h1 class="text-xl font-bold">Message</h1>
    </div>    
    <section class="">
      <div class="py-5 px-2">
        <ul class="flex flex-col gap-3">
          <li>
            <nuxtLink to="/chat">
              <div class="flex gap-3 my-2">
                <div class="relative rounded-full overflow-hidden min-w-12 min-h-12 -z-2 -z-index-2">
                  <img 
                    class="w-full h-full absolute"
                    src="~/assets/img/avatar.jpg" 
                    alt="Dionísio Neto"
                  >
                </div>
                <div class="w-full">
                  <div class="flex justify-between items-center">
                    <div class="text-2xl font-bold">Dionísio Neto</div>
                    <div class="">11:30</div>
                  </div>
                  
                  <div class="flex items-center justify-between">
                    <div class="text-sm flex items-center gap-1"> <IconCheck :size="16"/> Boa noite</div><div class="text-xs bg-neutral-400 p-1 rounded-full w-5 h-5 flex justify-center items-center">3</div>
                  </div>  
                </div>
              </div>
              <hr class="ml-20 mr-5 border-1 border-neutral-700">
            </nuxtLink>
          </li>

          
        </ul>
      </div>
    </section>
</template>