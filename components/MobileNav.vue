<template>
  <nav class="bg-neutral-950 dark:bg-neutral-950 fixed bottom-0 w-full p-1 sm:hidden block">
    <ul class="flex justify-between items-center">
        <li>
          <NuxtLink 
            to="/" 
            active-class="bg-neutral-700/50"
            class="hover:dark:bg-neutral-700 hover:bg-neutral-300 p-2 rounded-md flex"
          >
            <IconHome :size="20"/>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink
            to="/message" 
            active-class="bg-neutral-700/50"
            class="hover:dark:bg-neutral-700 hover:bg-neutral-300 p-2 rounded-md flex"
          >
            <IconMessageSquare :size="20"/>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink 
            to="/stories" 
            active-class="bg-neutral-700/50"
            class="hover:dark:bg-neutral-700 hover:bg-neutral-300 p-2 rounded-md flex"
          >
            <IconShapes :size="20"/>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink 
            to="/notifications" 
            active-class="bg-neutral-700/50"
            class="hover:dark:bg-neutral-700 hover:bg-neutral-300 p-2 rounded-md flex"
          >
            <IconBell :size="20"/>
          </NuxtLink>
        </li>
        <li>
          <NuxtLink 
            to="/settings" 
            active-class="bg-neutral-700/50"
            class="hover:dark:bg-neutral-700 hover:bg-neutral-300 p-2 rounded-md flex"
          >
            <IconSettings :size="20"/>
          </NuxtLink>
        </li>
      </ul>
  </nav>
</template>