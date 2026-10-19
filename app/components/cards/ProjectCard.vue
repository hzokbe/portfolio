<script lang="ts" setup>
defineProps<{
  project: Project;
}>();
</script>

<template>
  <UCard :description="project.description" :title="project.title">
    <div>
      <img
        v-if="project.image"
        :alt="`Prévia do projeto ${project.title}`"
        :src="project.image"
        class="w-full h-full object-cover ring ring-default rounded-sm"
        loading="lazy"
      />
      <div
        v-else
        class="flex items-center justify-center bg-elevated rounded-sm min-h-48"
      >
        <UIcon class="size-12 text-muted" name="i-lucide-image" />
      </div>
    </div>
    <template #footer>
      <div class="flex flex-wrap gap-2">
        <UBadge
          v-for="technology in project.technologies"
          :key="technology"
          color="neutral"
          variant="subtle"
        >
          {{ technology }}
        </UBadge>
      </div>
      <div class="mt-3 flex flex-wrap gap-4">
        <UButton
          :to="project.repository"
          color="neutral"
          label="Ver repositório"
          rel="noopener noreferrer"
          target="_blank"
          trailing-icon="i-lucide-external-link"
          variant="outline"
        />
      </div>
    </template>
  </UCard>
</template>
