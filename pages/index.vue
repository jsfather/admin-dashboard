<script setup lang="ts">
import { useAutoAnimate } from '@formkit/auto-animate/vue'

const items = ref(["😏","😐","😑","😒","😕" ])
function removeItem(toRemove: any) {
  items.value = items.value.filter((item) => item !== toRemove)
}

const [parent] = useAutoAnimate()

</script>

<template>
  <h1 class="text-primary">Index Page</h1>
  <h5>Click emojis to remove them.</h5>
  <ul ref="parent" class="flex flex-row">
    <li
        v-for="item in items"
        :key="item"
        @click="removeItem(item)"
    >
      {{ item }}
    </li>
  </ul>
</template>

<style scoped>

</style>