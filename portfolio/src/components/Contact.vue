<template>
  <section id="contact" class="px-6 md:px-16 py-32 text-black dark:text-white">

    <h2 class="text-3xl mb-16 tracking-tight">
      {{ t.contactTitle }}
    </h2>

    <div class="space-y-6 text-gray-600 dark:text-gray-400">

      <a href="mailto:your@email.com" class="block hover:text-black dark:text-white transition">
        Email
      </a>

      <a href="https://github.com/yourgithub" target="_blank" class="block hover:text-black dark:text-white transition">
        GitHub
      </a>

      <a href="https://t.me/yourtelegram" target="_blank" class="block hover:text-black dark:text-white transition">
        Telegram
      </a>

    </div>

  </section>
</template>

<script setup>
defineProps(['t'])
</script>