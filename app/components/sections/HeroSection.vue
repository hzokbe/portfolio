<template>
  <UPageHero id="hero" class="min-h-dvh flex items-center">
    <template #title>
      <div class="flex flex-col items-center gap-4">
        <UAvatar
          :ui="{
            root: 'w-24 h-24 sm:w-48 sm:h-48',
          }"
          alt="Foto de Lucas Fernandes"
          icon="i-lucide-user"
          src="https://avatars.githubusercontent.com/u/211994572"
        />
        <h1 class="text-4xl sm:text-6xl font-bold">Lucas Fernandes</h1>
      </div>
    </template>
    <template #description>
      <p class="text-xl text-muted max-w-xl mx-auto">
        Desenvolvedor de Software apaixonado por tecnologia, arquitetura de
        sistemas e criação de aplicações úteis.
      </p>
    </template>
    <template #links>
      <SocialLinks />
    </template>
  </UPageHero>
</template>
