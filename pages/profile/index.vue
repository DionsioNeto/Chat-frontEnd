<script setup>
useHead({
  title: "Dionísio | TMJ",
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
    <h1 class="text-xl font-bold">
      Dionísio Neto <IconBadgeCheck class="inline text-blue-500" :size="18"/>
    </h1>
  </div>    
  <section class="py-3">
    <div class="bg-neutral-900 w-fll h-36 rounded-lg"></div>
    <div class="flex justify-between items-center mb-2">
      <div class="border-2 border-neutral-950 -mt-8 ml-2 relative rounded-full overflow-hidden w-24 h-24 -z-2 -z-index-2">
        <img 
          class="w-full h-full absolute"
          src="~/assets/img/avatar.jpg" 
          alt="Dionísio Neto"
        >
      </div>
      <div class="bg-neutral-800 rounded-full p-2 border-2 border-neutral-700">
        <IconShare/>
      </div>
    </div>
    <div class="flex flex-col gap-2">
      <h2 class="text-2xl font-bold">Dionísio Neto <IconBadgeCheck class="inline text-blue-500" :size="18"/></h2>
      <div class="text-neutral-700 text-sm">@dionisio.neto14</div>
      <div class="text-neutral-500 text-sm"><IconCalendarDays class="inline" :size="18"/> Since 2025</div>
      <div class="text-neutral-500 text-sm"><IconLink2 class="inline"/> https://dionisio-neto.netlify.app/</div>
      <p class="max-w-[80%]">
        Lorem ipsum dolor sit amet consectetur adipisicing elit. Amet nobis vitae atque quos necessitatibus, fugiat dolorem id reprehenderit.
      </p>
      <div class="flex gap-2">
        <button class="bg-neutral-200 text-black rounded-lg p-1"> <IconUserPen class="inline"/> Edit profile</button>
        <button class="border rounded-lg p-1"> <IconUsers class="inline"/> Manager your contact</button>
      </div>
    </div>
    
  </section>
</template>