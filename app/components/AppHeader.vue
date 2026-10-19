<script lang="ts" setup>
import type { NavigationMenuItem } from '@nuxt/ui';

const navigationLinks: NavigationMenuItem[] = [
  { label: 'Sobre', to: '#about', icon: 'i-lucide-user' },
  {
    label: 'Habilidades',
    to: '#skills',
    icon: 'i-lucide-wrench',
  },
  {
    label: 'Projetos',
    to: '#projects',
    icon: 'i-lucide-folders',
  },
];
</script>

<template>
  <UHeader title="Lucas Fernandes" to="#hero">
    <UNavigationMenu :items="navigationLinks" variant="link" />
    <template #right>
      <UColorModeButton />
    </template>
    <template #body>
      <UNavigationMenu
        :items="navigationLinks"
        class="-mx-2.5"
        orientation="vertical"
      />
    </template>
  </UHeader>
</template>
