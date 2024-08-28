<script lang="ts" setup>
definePageMeta({
  middleware: 'verified',
})

const title = 'Secret'

useSeoMeta({
  title,
})
</script>

<template>
  <UContainer>
    <UPage>
      <UPageHeader
        :title
      />
      <UPageBody>
        <h1 class="text-blue-600 dark:text-blue-300">
          Miejsce i treści sekretne - tylko dla zalogowanych
        </h1>
      </UPageBody>
      <!-- Use a UPageBody to build the user dashboard -->
    </UPage>
  </UContainer>
</template>
