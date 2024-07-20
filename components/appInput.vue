<script setup lang="ts">
withDefaults(
    defineProps<{
      prependIcon?: boolean;
    }>(),
    {
      prependIcon: false
    },
);
</script>

<template>
  <div class="relative my-auto">
    <div v-if="prependIcon" class="absolute inset-y-0 start-0 flex items-center ps-3 pointer-events-none">
      <slot name="prependIcon"/>
    </div>
    <input
        v-bind="$attrs"
        type="search" id="default-search"
        class="block w-full p-3 text-sm bg-background rounded-xl focus:outline-none"
        :class="{ 'ps-10': prependIcon }"
    />
  </div>
</template>

<style scoped>

</style>