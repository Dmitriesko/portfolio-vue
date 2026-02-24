<template>
  <section id="projects" class="px-6 md:px-16 py-32 text-black dark:text-white">

    <h2 class="text-3xl mb-16 tracking-tight">
      {{ t.projectsTitle }}
    </h2>

    <div class="space-y-10 text-gray-600 dark:text-gray-400">

      <div class="hover:text-black dark:text-white transition">
        <a href="https://github.com/yourgithub/project1" target="_blank">
          CRM System — Laravel, Vue, MySQL
        </a>
      </div>

      <div class="hover:text-black dark:text-white transition">
        <a href="https://github.com/yourgithub/project2" target="_blank">
          Blog Platform — REST API, Auth, Admin Panel
        </a>
      </div>

    </div>

  </section>
</template>

<script setup>
defineProps(['t'])
</script>
