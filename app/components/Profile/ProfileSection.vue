<script lang="ts" setup>
defineProps<{
  title: string
  description: string
  bio: string
}>()
</script>

<template>
  <section class="flex flex-col gap-6 md:flex-row md:gap-16">
    <div class="space-y-1 w-[28rem] shrink-0">
      <h2 class="text-md font-bold">
        {{ title }}
      </h2>
      <h3 class="text-gray-500 dark:text-gray-400">
        {{ description }}
      </h3>
      <h4 class="text-orange-800 dark:text-orange-300">
        {{ bio }}
      </h4>
    </div>

    <slot />
  </section>
</template>
