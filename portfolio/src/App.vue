<template>
  <div class="bg-white text-black dark:bg-[#0f0f0f] dark:text-white transition-colors duration-500">

    <!-- Theme Toggle -->
    <div class="fixed top-6 left-6 text-sm uppercase tracking-widest">
      <button @click="toggleTheme" class="hover:opacity-60 transition">
        {{ isDark ? 'Light' : 'Dark' }}
      </button>
    </div>

    <Hero
        :t="t"
        :language="language"
        :setLanguage="setLanguage"
    />

    <Projects :t="t" />
    <Contact :t="t" />

  </div>
</template>

<script setup>
import { ref, computed, watch } from 'vue'
import { content } from './content/content'
import Hero from './components/Hero.vue'
import Projects from './components/Projects.vue'
import Contact from './components/Contact.vue'

const language = ref('ru')
const isDark = ref(true)

const t = computed(() => content[language.value])

function setLanguage(lang) {
  language.value = lang
}

function toggleTheme() {
  isDark.value = !isDark.value
}

watch(isDark, (val) => {
  if (val) {
    document.documentElement.classList.add('dark')
  } else {
    document.documentElement.classList.remove('dark')
  }
})
</script>