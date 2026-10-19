<script lang="ts" setup>
import { skillGroups } from '~/data/skills';
</script>

<template>
  <UPageSection
    id="skills"
    class="min-h-dvh flex items-center"
    title="Habilidades"
  >
    <div class="grid grid-cols-1 gap-8 sm:grid-cols-2 max-w-3xl mx-auto">
      <div v-for="group in skillGroups" :key="group.title" class="space-y-3">
        <h3 class="text-lg font-semibold">{{ group.title }}</h3>
        <ul class="flex flex-wrap gap-2">
          <li v-for="skill in group.skills" :key="skill.name">
            <UBadge
              :icon="skill.icon"
              :label="skill.name"
              color="neutral"
              size="lg"
              variant="outline"
            />
          </li>
        </ul>
      </div>
    </div>
  </UPageSection>
</template>
