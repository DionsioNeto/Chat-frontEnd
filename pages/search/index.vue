<script setup>
useHead({
  title: "Search | TMJ",
  meta: [{
      name: "description",
      content: "some description"
      },
  ]
})
</script>
<template>

    <div class="dark:text-neutral-300 flex gap-5 items-center border-2 border-neutral-700 p-3 rounded-xl sticky top-0 bg-neutral-950 z-30">
      <h1 class="text-xl font-bold">Search</h1>
    </div>    
    <section class="my-3 h-80"> 
      <label for="search">
        <div class="bg-neutral-900 rounded-xl border-2 border-neutral-700 py-1 px-2  dark:text-neutral-400">
          <form class="flex justify-between items-center gap-2">
            <div class="flex gap-1 items-center w-full">
              <IconSearch/>
              <input 
                id="search"
                placeholder="Search ..."
                class="bg-transparent w-full outline-none"
              />
            </div>
            <IconX :size="15"/>
          </form>
        </div>
      </label>
      <div class="py-5 px-2">
        <ul class="flex flex-col gap-3">
          <li>
            <nuxtLink to="/profile">
              <div class="flex gap-3 my-2">
                <div class="relative rounded-full overflow-hidden w-12 h-12 -z-2 -z-index-2">
                  <img 
                    class="w-full h-full absolute"
                    src="~/assets/img/avatar.jpg" 
                    alt="Dionísio Neto"
                  >
                </div>
                <div class="">
                  <div class="text-2xl font-bold">Dionísio Neto
                    <IconBadgeCheck class="inline text-blue-500" :size="18"/>
                  </div>
                  <div class="text-neutral-700 text-sm">@dionisio.neto14</div>
                </div>
              </div>
              <hr class="ml-20 mr-5 border-1 border-neutral-700">
            </nuxtLink>
          </li>

          <li>
            <nuxtLink to="/profile">
              <div class="flex gap-3 my-2">
                <div class="relative rounded-full overflow-hidden w-12 h-12 -z-2 -z-index-2">
                  <img 
                    class="w-full h-full absolute"
                    src="~/assets/img/avatar.jpg" 
                    alt="Dionísio Neto"
                  >
                </div>
                <div class="">
                  <div class="text-2xl font-bold">Dionísio Neto</div>
                  <div class="text-neutral-700 text-sm">@dionisio.neto14</div>
                </div>
              </div>
              <hr class="ml-20 mr-5 border-1 border-neutral-700">
            </nuxtLink>
          </li>
          
        </ul>
      </div>
    </section>
  
</template>