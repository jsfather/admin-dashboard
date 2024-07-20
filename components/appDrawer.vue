<script setup lang="ts">
const items = [{title: 'About'}, {title: 'Services'}, {title: 'Clients'}, {title: 'Contact'}]
</script>

<template>
  <div class="w-64 fixed top-0 h-full bg-base p-2 shadow-lg">
    <a v-for="item in items" href="#" class="block rounded-2xl hover:text-primary hover:bg-background py-3 px-4">{{
        item.title
      }}</a>
  </div>
</template>

<style scoped>

</style>