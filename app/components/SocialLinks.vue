<script lang="ts" setup>
import { socials } from '~/data/socials';
</script>

<template>
  <div class="flex flex-wrap justify-center gap-2">
    <UButton
      v-for="social in socials"
      :key="social.label"
      :icon="social.icon"
      :label="social.label"
      :to="social.url"
      color="neutral"
      rel="noopener noreferrer"
      size="lg"
      target="_blank"
      variant="outline"
    />
  </div>
</template>
