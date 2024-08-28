<script lang="ts" setup>
const title = useRuntimeConfig().app.name

const appConfig = useAppConfig()
const notice = appConfig.footer.notice
const smallLinks = appConfig.footer.smallLinks
const socials = appConfig.socials
</script>

<template>
  <UFooter
    :links="smallLinks"
    :ui="{ bottom: { left: 'text-sm text-gray-600 dark:text-orange-300' } }"
  >
    <template #left>
      {{ title }} - {{ notice }}
    </template>

    <template #right>
      Copyright © {{ new Date().getFullYear() }}
      <UButton
        v-for="social in socials"
        :key="social.title"
        square
        color="green"
        variant="ghost"
        v-bind="social"
      />
    </template>
  </UFooter>
</template>
