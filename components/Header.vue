<script setup lang="ts">
</script>
<template>
  <header class="sticky top-2 flex justify-between items-center mx-2 mb-0 bg-neutral-200 dark:bg-neutral-800 p-2 rounded-lg h-13">
    <Logo />
    <label for="search">
      <form action="" method="post" class="flex gap-2 items-center bg-neutral-300 dark:bg-neutral-900 rounded-full p-2">
        <button>
          <IconSearch :size="20"/>
        </button>
        <input id="search" type="text" placeholder="Search..." class="bg-neutral-300 dark:bg-neutral-900 outline-none">
      </form>
    </label>
  </header>
</template>