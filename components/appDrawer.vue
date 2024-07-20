<script setup lang="ts">
const items = [
  {title: 'About', icon: 'mage:dashboard-2'},
  {title: 'Services', icon: 'mage:dashboard-2'},
  {title: 'Clients', icon: 'mage:dashboard-2'},
  {title: 'Contact', icon: 'mage:dashboard-2'}
]
</script>

<template>
  <div class="w-64 fixed top-0 h-full bg-base p-2 shadow-lg">
    <a v-for="item in items" href="#" class="block rounded-2xl hover:text-primary hover:bg-background py-3 px-4">
      <Icon :name="item.icon" class="text-opposite hover:text-primary"/>
      {{
        item.title
      }}</a>
  </div>
</template>

<style scoped>

</style>