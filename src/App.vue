<script setup lang="ts">
import Header from './components/Header.vue'
import About from './components/About.vue'
import Experience from './components/Experience.vue'
import Education from './components/Education.vue'
import Skills from './components/Skills.vue'
import Projects from './components/Projects.vue'
</script>

<template>
  <div class="min-h-screen bg-gradient-to-br from-indigo-50 via-purple-50 to-pink-50">
    <Header />
    <main class="max-w-4xl mx-auto p-4 md:p-8 space-y-6">
      <About />
      <Projects />
      <div class="grid md:grid-cols-2 gap-6">
        <Experience />
        <div class="space-y-6">
          <Education />
          <Skills />
        </div>
      </div>
    </main>
  </div>
</template>