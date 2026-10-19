<script lang="ts" setup>
import HeroSection from '~/components/sections/HeroSection.vue';
import ProjectsSection from '~/components/sections/ProjectsSection.vue';
import SkillsSection from '~/components/sections/SkillsSection.vue';
import AboutSection from '~/components/sections/AboutSection.vue';

const title = 'Lucas Fernandes - Desenvolvedor de Software';

const description =
  'Portfólio de Lucas Fernandes, desenvolvedor de software com foco em aplicações web completas, arquitetura de sistemas e boas práticas.';

useHead({
  htmlAttrs: { lang: 'pt-BR' },
});

useSeoMeta({
  title,
  description,
});
</script>

<template>
  <div class="flex flex-col">
    <HeroSection />
    <USeparator />
    <AboutSection />
    <USeparator />
    <SkillsSection />
    <USeparator />
    <ProjectsSection />
  </div>
</template>
