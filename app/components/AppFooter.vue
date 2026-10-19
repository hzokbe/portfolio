<script lang="ts" setup>
import { socials } from '~/data/socials';

const year = new Date().getFullYear();
</script>

<template>
  <UFooter>
    <template #left>
      <p class="text-sm text-muted">© {{ year }} Lucas Fernandes</p>
    </template>
    <template #right>
      <UButton
        v-for="social in socials"
        :key="social.label"
        :aria-label="social.label"
        :icon="social.icon"
        :to="social.url"
        color="neutral"
        rel="noopener noreferrer"
        target="_blank"
        variant="ghost"
      />
    </template>
  </UFooter>
</template>
