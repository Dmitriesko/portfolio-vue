<template>
  <div class="min-h-screen px-6 md:px-16 text-black dark:text-white">

    <div class="flex justify-end pt-8 text-sm uppercase tracking-widest">
      <button
          @click="setLanguage('ru')"
          :class="language === 'ru' ? 'text-black dark:text-white' : 'text-gray-500'"
          class="mr-4 transition"
      >
        RU
      </button>

      <button
          @click="setLanguage('en')"
          :class="language === 'en' ? 'text-black dark:text-white' : 'text-gray-500'"
          class="transition"
      >
        EN
      </button>
    </div>

    <section class="flex flex-col justify-center h-[80vh] animate-fade">

      <h1 class="text-5xl md:text-7xl font-semibold tracking-tight leading-tight">
        Barbara
      </h1>

      <p class="text-gray-600 dark:text-gray-400 text-xl mt-6">
        {{ t.role }}
      </p>

      <p class="text-gray-500 text-lg mt-6 max-w-xl">
        {{ t.description }}
      </p>

      <div class="mt-10 flex gap-8 text-sm uppercase tracking-widest">
        <a href="#projects" class="hover:text-gray-600 dark:text-gray-400 transition">
          {{ t.projectsTitle }}
        </a>
        <a href="#contact" class="hover:text-gray-600 dark:text-gray-400 transition">
          {{ t.contactTitle }}
        </a>
      </div>

    </section>
  </div>
</template>

<script setup>
defineProps(['t', 'language', 'setLanguage'])
</script>

<style>
@keyframes fade {
  from {
    opacity: 0;
    transform: translateY(25px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}

.animate-fade {
  animation: fade 1s ease forwards;
}
</style>