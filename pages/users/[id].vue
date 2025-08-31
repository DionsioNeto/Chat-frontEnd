<template>
  <h1 class="text-3xl">Users</h1>
  User: {{ route.params.id }}
</template>
<script setup>
const route = useRoute()
</script>