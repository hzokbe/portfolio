<script lang="ts" setup>
import { projects } from '~/data/projects';
import ProjectCard from '~/components/cards/ProjectCard.vue';
</script>

<template>
  <UPageSection
    id="projects"
    class="min-h-dvh flex items-center"
    description="Alguns projetos pessoais em que aplico meus conhecimentos e exploro novas tecnologias."
    title="Projetos"
  >
    <UPageGrid class="grid-cols-1 md:grid-cols-2">
      <ProjectCard
        v-for="project in projects"
        :key="project.title"
        :project="project"
      />
    </UPageGrid>
  </UPageSection>
</template>
